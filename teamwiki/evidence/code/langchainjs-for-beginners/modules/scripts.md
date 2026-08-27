---
title: langchainjs-for-beginners — scripts module
domain: code-knowledge
source: [scripts/]
---

# scripts

**28 facts** (component: 17, config: 9, interface: 1, error: 1)

## Core components

- `createChatModel` ← scripts/create-model.ts:23
- `createEmbeddingsModel` ← scripts/create-model.ts:40
- `TestResult` ← scripts/validation-common.ts:12
- `INTERACTIVE_FILES` ← scripts/validation-common.ts:20
- `SERVER_FILES` ← scripts/validation-common.ts:29
- `SKIP_FILES` ← scripts/validation-common.ts:49
- `TIMEOUT_MS` ← scripts/validation-common.ts:59
- `findCodeFiles` ← scripts/validation-common.ts:91
- `getInteractiveInput` ← scripts/validation-common.ts:121
- `getServerConfig` ← scripts/validation-common.ts:129
- `shouldSkipFile` ← scripts/validation-common.ts:136
- `getSkipReason` ← scripts/validation-common.ts:143
- `runServerExample` ← scripts/validation-common.ts:151
- `runExample` ← scripts/validation-common.ts:319
- `findChapters` ← scripts/validation-common.ts:343
- `collectAllCodeFiles` ← scripts/validation-common.ts:357
- `displayTestSummary` ← scripts/validation-common.ts:387
- `displayFinalResults` ← scripts/validation-common.ts:416

## Config

- `process.env.AI_MODEL` ← scripts/create-model.ts
- `process.env.AI_ENDPOINT` ← scripts/create-model.ts
- `process.env.AI_API_KEY` ← scripts/create-model.ts
- `process.env.AI_EMBEDDING_MODEL` ← scripts/create-model.ts
- `process.env.AI_API_KEY` ← scripts/test-setup.ts
- `process.env.AI_ENDPOINT` ← scripts/test-setup.ts
- `process.env.AI_MODEL` ← scripts/test-setup.ts
- `process.env.VALIDATION_CONCURRENCY` ← scripts/validate-examples-parallel.ts
- `process.env.VALIDATION_RETRIES` ← scripts/validation-common.ts

## Errors

- `RETRYABLE_ERROR_PATTERNS` ← scripts/validation-common.ts
