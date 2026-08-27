# Test Rule (TeamAI)

This is a **smoke-test rule** to verify TeamAI rule sync (`teamai push` / `teamai pull`). It is not a production coding standard.

## When this rule is loaded

If the user asks whether project rules are working, or mentions `test-rule` / `TEAMAI_TEST_RULE`, reply with exactly:

`TEAMAI_TEST_RULE_OK`

Then add one short sentence that this confirmation came from `.cursor/rules/common/test-rule.md`.

## Do not

- Do not apply this rule to unrelated coding tasks.
- Do not treat this file as a required style guide for the course examples.
