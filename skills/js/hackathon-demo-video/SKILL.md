---
name: hackathon-demo-video
description: >-
  Produce a short hackathon demo video of a web app with Playwright (hook,
  problem, live demo, impact). Use when the user asks for a hackathon demo,
  pitch video, judge walkthrough, 60–90s product recording, or demo day clip.
metadata:
  origin: local
---

# Hackathon Demo Video

Record a **judge-ready** product clip: one golden path, visible cursor, captions, strict time box. Default stack: Playwright + Chromium, output WebM 1280×720.

This is not a tutorial and not a slide deck. Judges watch dozens of videos. The first 8 seconds must land the problem and the wow.

## When to Use

- User asks for a hackathon / demo-day / pitch / 评委演示 video
- Need a 60–90s (max 3 min) recording of a working web UI
- User wants subtitles, a storyboard, or a “show the product, not the slides” clip

If they only want a long product walkthrough, still use this narrative, then trim.

## Constraints (do not violate)

| Rule | Default |
|------|---------|
| Length | **75s target**, 60–90s OK, **hard cap 180s** |
| Aspect | 16:9, `1280x720` (1080p only if they ask) |
| Audio | Captions required (judging rooms are often muted) |
| Path | **One** happy path. No settings, no errors, no signup |
| Auth | Pre-seed logged-in / demo data. Never film a login form unless that *is* the product |
| Talking | Optional VO script; video must stand alone with subtitles |

## Deliverables

1. `storyboard.md` — timed beats + subtitle lines
2. `demo-hackathon.cjs` — Playwright script (`--rehearse` then record)
3. Video file with a **stable name**: `hackathon-demo-<project>.webm`
4. End card text: project name, one-line value, team, URL/repo

---

## Phase 0: Lock the pitch (before any browser)

Ask only what you cannot infer from the repo/README. Then write the storyboard.

### Narrative (fixed order)

1. **Hook (0–8s)** — Who hurts, how badly, in one sentence. No logo linger.
2. **Promise (8–15s)** — Name the product and the one capability that wins.
3. **Live demo (15–65s)** — 3–5 clicks. The **wow moment** is in the middle, not the end.
4. **Proof (65–75s)** — Result on screen (list, chart, generated artifact, money/time saved).
5. **Close (last 5–8s)** — End card: name + one-liner + how to try.

### Pick one wow moment

Write it as a single sentence before scripting:

```text
WOW: When the user does X, the UI shows Y in <3s, which previously took Z.
```

Everything that does not serve this sentence is cut.

### Time budget (75s)

```text
0:00  Hook subtitle + land on the painful empty/broken state OR the app home
0:08  Product name + promise
0:15  First action (type/click) — cursor moves, no teleport
0:35  Wow moment — hold 2–3s so judges can read the result
0:50  One reinforcing detail (optional; cut if over time)
1:05  Full-screen result
1:10  End card
1:15  Cut
```

### Subtitle rules

- One line, **≤ 40 Chinese chars or ≤ 60 Latin chars**
- Format: `问题 / 动作 / 结果`，not “Step 1 - …”
- Must be readable muted
- Chinese default; add English only if the user says the hackathon is EN

Example beats:

```text
00:00  客服工单堆积，平均要 20 分钟才分到人
00:08  TicketPilot 用对话自动分流并起草回复
00:16  粘贴一封愤怒邮件
00:28  三秒给出优先级、负责组和回复草稿
00:48  一键发送，工单从「待处理」变成「已响应」
01:08  TicketPilot · 让一线客服把时间花在真正难的单上
```

Do **not** start recording until the user confirms the wow sentence and the beat list (or they said “just record”).

---

## Phase 1: Discover

Start the app. Open every screen in the golden path. Dump real controls — do not guess `<input>` vs `<textarea>` vs custom combobox.

```javascript
const fields = await page.evaluate(() => {
  const els = [];
  document.querySelectorAll('input, select, textarea, button, a, [contenteditable], [role="button"]').forEach((el) => {
    if (el.offsetParent === null) return;
    els.push({
      tag: el.tagName,
      type: el.type || '',
      name: el.name || '',
      placeholder: el.placeholder || '',
      text: (el.textContent || '').trim().slice(0, 40),
      href: el.getAttribute('href') || '',
      role: el.getAttribute('role') || '',
    });
  });
  return els;
});
console.log(JSON.stringify(fields, null, 2));
```

Pre-seed:

- Demo user already logged in (storageState, query flag, or local seed script)
- Sample data that makes the wow obvious (before/after contrast)
- Disable toasts that cover the subtitle bar; hide “dev” banners if they clutter

---

## Phase 2: Rehearse

`--rehearse` with **no** `recordVideo`. Fail loud if a selector is missing.

```javascript
async function ensureVisible(page, locator, label) {
  const el = typeof locator === 'string' ? page.locator(locator).first() : locator;
  const visible = await el.isVisible().catch(() => false);
  if (!visible) {
    console.error(`REHEARSAL FAIL: "${label}"`);
    const found = await page.evaluate(() =>
      Array.from(document.querySelectorAll('button, input, select, textarea, a'))
        .filter((n) => n.offsetParent !== null)
        .map((n) => `${n.tagName} "${(n.textContent || n.placeholder || '').trim().slice(0, 30)}"`)
        .join('\n  ')
    );
    console.error('  Visible:\n  ' + found);
    return false;
  }
  console.log(`REHEARSAL OK: "${label}"`);
  return true;
}
```

Re-run until every beat’s selector passes. Then record.

---

## Phase 3: Record

Headless Chromium, `1280x720`. Re-inject cursor + subtitle **after every navigation**.

### Pacing (hackathon is tighter than tutorials)

- After navigation: `2s` (not 4s)
- After click: `1.2–1.8s`
- After wow result: **`2.5–3s` hold**
- Typing: `28–40ms` / char; shorten sample text so typing does not eat the budget
- Never teleport the mouse (`mouse.move` with `steps: 8–12` then click)

### Helpers (required)

Paste these into the script (same behavior every time):

**Cursor** — SVG arrow, `position: fixed`, `z-index: 999999`, `pointer-events: none`. Re-inject on navigate.

**moveAndClick** — `scrollIntoViewIfNeeded` → move to box center → pause 300–400ms → click → `postClickDelay`. Log and skip if not visible; never silent `catch`.

**typeSlowly** — moveAndClick → `fill('')` → `pressSequentially` with delay.

**Subtitles** — bottom bar `rgba(0,0,0,0.75)`, 16px, z-index just under cursor. `showSubtitle(page, text)` / clear with `''`.

**End card** — last navigation or an injected full-viewport overlay (dark bg, product name, one-liner, URL). Hold 5–8s.

Cursor + subtitle snippets:

```javascript
async function injectCursor(page) {
  await page.evaluate(() => {
    if (document.getElementById('demo-cursor')) return;
    const cursor = document.createElement('div');
    cursor.id = 'demo-cursor';
    cursor.innerHTML = `<svg width="24" height="24" viewBox="0 0 24 24" fill="none"><path d="M5 3L19 12L12 13L9 20L5 3Z" fill="white" stroke="black" stroke-width="1.5" stroke-linejoin="round"/></svg>`;
    cursor.style.cssText = 'position:fixed;z-index:999999;pointer-events:none;width:24px;height:24px;transition:left .1s,top .1s;filter:drop-shadow(1px 1px 2px rgba(0,0,0,.3));left:0;top:0';
    document.body.appendChild(cursor);
    document.addEventListener('mousemove', (e) => {
      cursor.style.left = e.clientX + 'px';
      cursor.style.top = e.clientY + 'px';
    });
  });
}

async function injectSubtitleBar(page) {
  await page.evaluate(() => {
    if (document.getElementById('demo-subtitle')) return;
    const bar = document.createElement('div');
    bar.id = 'demo-subtitle';
    bar.style.cssText = 'position:fixed;bottom:0;left:0;right:0;z-index:999998;text-align:center;padding:12px 24px;background:rgba(0,0,0,.75);color:#fff;font-family:-apple-system,"Segoe UI",sans-serif;font-size:16px;font-weight:500;pointer-events:none;opacity:0;transition:opacity .3s';
    document.body.appendChild(bar);
  });
}

async function showSubtitle(page, text) {
  await page.evaluate((t) => {
    const bar = document.getElementById('demo-subtitle');
    if (!bar) return;
    bar.textContent = t;
    bar.style.opacity = t ? '1' : '0';
  }, text);
  if (text) await page.waitForTimeout(500);
}

async function showEndCard(page, { title, line, url }) {
  await page.evaluate(({ title, line, url }) => {
    const el = document.createElement('div');
    el.id = 'demo-endcard';
    el.style.cssText = 'position:fixed;inset:0;z-index:999997;background:#0b0b0f;color:#fff;display:flex;flex-direction:column;align-items:center;justify-content:center;font-family:-apple-system,"Segoe UI",sans-serif;text-align:center;padding:24px';
    el.innerHTML = `<div style="font-size:36px;font-weight:700">${title}</div><div style="margin-top:16px;font-size:20px;opacity:.9;max-width:720px">${line}</div><div style="margin-top:28px;font-size:16px;opacity:.7">${url}</div>`;
    document.body.appendChild(el);
  }, { title, line, url });
  await page.waitForTimeout(6000);
}
```

### Script skeleton

```javascript
'use strict';
const { chromium } = require('playwright');
const path = require('path');
const fs = require('fs');

const BASE_URL = process.env.DEMO_BASE_URL || 'http://localhost:3000';
const VIDEO_DIR = path.join(__dirname, 'hackathon-demo');
const OUTPUT_NAME = 'hackathon-demo-PROJECT.webm';
const REHEARSAL = process.argv.includes('--rehearse');

(async () => {
  const browser = await chromium.launch({ headless: true });
  const viewport = { width: 1280, height: 720 };

  if (REHEARSAL) {
    const context = await browser.newContext({ viewport });
    const page = await context.newPage();
    await page.goto(BASE_URL);
    // ensureVisible for every selector in the golden path
    await browser.close();
    return;
  }

  fs.mkdirSync(VIDEO_DIR, { recursive: true });
  const context = await browser.newContext({
    recordVideo: { dir: VIDEO_DIR, size: viewport },
    viewport,
    // storageState: 'demo-auth.json', // prefer this over filming login
  });
  const page = await context.newPage();

  try {
    await page.goto(BASE_URL);
    await injectCursor(page);
    await injectSubtitleBar(page);
    await showSubtitle(page, '…hook…');
    // golden path: moveAndClick / typeSlowly only
    await showSubtitle(page, '');
    await showEndCard(page, {
      title: 'ProjectName',
      line: 'One-line value',
      url: 'https://example.com',
    });
  } catch (err) {
    console.error('DEMO ERROR:', err.message);
  } finally {
    await context.close();
    const video = page.video();
    if (video) {
      const src = await video.path();
      const dest = path.join(VIDEO_DIR, OUTPUT_NAME);
      fs.copyFileSync(src, dest);
      console.log('Video saved:', dest);
    }
    await browser.close();
  }
})();
```

```bash
npx playwright install chromium   # once
node demo-hackathon.cjs --rehearse
node demo-hackathon.cjs
```

If duration is over 90s: cut the reinforcing beat, shorten typed strings, reduce post-click delays. Do not speed up the wow hold.

---

## Quality bar

Watch the file (or step through timestamps). Reject and re-record if any fail:

- [ ] Opens on pain or promise, not a blank spinner
- [ ] Wow moment is on screen ≥ 2.5s
- [ ] Cursor is an arrow and never jumps
- [ ] Subtitles match the storyboard and never cover the wow UI (if they do, raise the bar or scroll)
- [ ] No login, 404, cookie banner, or `localhost` debug overlay in frame
- [ ] End card is readable
- [ ] Filename is stable, not Playwright’s random id

## Pitfalls

1. Tutorial pacing (too slow) — hackathon clips die after 20s of “welcome”.
2. Feature tour — one path, one wow.
3. Filming `npm start` / terminal — product UI only.
4. Cursor gone after `goto` — re-inject.
5. Subtitles in English while the UI is Chinese (or the reverse) — match the judging language.
6. Typing a paragraph — use a short paste-sized string.
7. Popup windows — capture the page explicitly; do not assume the opener video includes them.
