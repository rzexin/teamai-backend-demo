---
title: langchainjs-for-beginners config
domain: code-knowledge
source:
  - 06-mcp/code/03-mcp-multi-server.ts
  - 06-mcp/samples/basic-mcp-server.ts
  - 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-server.ts
  - scripts/create-model.ts
  - scripts/test-setup.ts
  - scripts/validate-examples-parallel.ts
  - scripts/validation-common.ts
  - 01-introduction/code/01-hello-world.ts
  - 01-introduction/code/02-message-types.ts
  - 01-introduction/code/03-model-comparison.ts
  - 01-introduction/samples/qa-program.ts
  - 01-introduction/solution/model-performance.ts
  - 01-introduction/solution/personality-test.ts
  - 02-chat-models/code/01-multi-turn.ts
  - 02-chat-models/code/02-streaming.ts
  - 02-chat-models/code/03-parameters.ts
  - 02-chat-models/code/04-init-chat-model.ts
  - 02-chat-models/code/05-error-handling.ts
  - 02-chat-models/code/06-token-tracking.ts
  - 02-chat-models/samples/robust-chat.ts
  - 02-chat-models/samples/streaming-chat.ts
  - 02-chat-models/samples/token-tracker.ts
  - 02-chat-models/solution/chatbot.ts
  - 02-chat-models/solution/temperature-lab.ts
  - 03-prompts-messages-outputs/code/01-messages-vs-templates.ts
  - 03-prompts-messages-outputs/code/02-message-construction.ts
  - 03-prompts-messages-outputs/code/03-basic-template.ts
  - 03-prompts-messages-outputs/code/04-template-formats.ts
  - 03-prompts-messages-outputs/code/05-few-shot.ts
  - 03-prompts-messages-outputs/code/06-composition.ts
  - 03-prompts-messages-outputs/code/07-structured-output.ts
  - 03-prompts-messages-outputs/code/08-zod-schemas.ts
  - 03-prompts-messages-outputs/samples/email-generator.ts
  - 03-prompts-messages-outputs/samples/prompt-builder.ts
  - 03-prompts-messages-outputs/samples/template-library.ts
  - 03-prompts-messages-outputs/samples/translator.ts
  - 03-prompts-messages-outputs/solution/format-teacher.ts
  - 03-prompts-messages-outputs/solution/product-extractor.ts
  - 04-function-calling-tools/code/02-tool-calling.ts
  - 04-function-calling-tools/code/03-tool-execution.ts
  - 04-function-calling-tools/code/04-multiple-tools.ts
  - 04-function-calling-tools/solution/travel-assistant.ts
  - 04-function-calling-tools/solution/weather-tool.ts
  - 05-agents/code/01-create-agent-basic.ts
  - 05-agents/code/02-create-agent-multi-tool.ts
  - 05-agents/code/03-agent-with-middleware.ts
  - 05-agents/code/04-builtin-middleware.ts
  - 05-agents/samples/basic-agent-manual-loop.ts
  - 05-agents/samples/multi-tool-agent-manual.ts
  - 05-agents/solution/planning-agent.ts
  - 05-agents/solution/research-agent.ts
  - 06-mcp/code/01-mcp-integration.ts
  - 06-mcp/code/02-mcp-stdio-local.ts
  - 06-mcp/code/04-mcp-error-handling.ts
  - 06-mcp/solution/context7-basic.ts
  - 06-mcp/solution/multi-server-integration.ts
  - 06-mcp/solution/multi-tool-agent.ts
  - 07-documents-embeddings-semantic-search/code/05-basic-embeddings.ts
  - 07-documents-embeddings-semantic-search/code/06-vector-store.ts
  - 07-documents-embeddings-semantic-search/code/07-similarity-scores.ts
  - 07-documents-embeddings-semantic-search/code/08-batch-embeddings.ts
  - 07-documents-embeddings-semantic-search/code/09-embedding-relationships.ts
  - 07-documents-embeddings-semantic-search/samples/embedding-visualizer.ts
  - 07-documents-embeddings-semantic-search/samples/multilingual-search.ts
  - 07-documents-embeddings-semantic-search/samples/search-comparison.ts
  - 07-documents-embeddings-semantic-search/solution/book-search.ts
  - 07-documents-embeddings-semantic-search/solution/similarity-explorer.ts
  - 08-agentic-rag-systems/code/01-when-to-use-rag.ts
  - 08-agentic-rag-systems/code/01a-traditional-rag.ts
  - 08-agentic-rag-systems/code/02-agentic-rag.ts
  - 08-agentic-rag-systems/samples/citation-rag.ts
  - 08-agentic-rag-systems/samples/multi-source-rag.ts
  - 08-agentic-rag-systems/solution/conversational-rag.ts
  - 08-agentic-rag-systems/solution/knowledge-base-rag.ts
  - 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-agent.ts
---

# Config

- `process.env.AI_MODEL` ← 06-mcp/code/03-mcp-multi-server.ts:67 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/code/03-mcp-multi-server.ts:68 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/code/03-mcp-multi-server.ts:69 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY
  ```
- `process.env.PORT` ← 06-mcp/samples/basic-mcp-server.ts:214 [EXTRACTED]
  ```
  const PORT = process.env.PORT || 3000;
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-server.ts:45 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-server.ts:46 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-server.ts:47 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← scripts/create-model.ts:25 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← scripts/create-model.ts:26 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← scripts/create-model.ts:27 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← scripts/create-model.ts:42 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_API_KEY` ← scripts/test-setup.ts:11 [EXTRACTED]
  ```
  if (!process.env.AI_API_KEY) {
  ```
- `process.env.AI_ENDPOINT` ← scripts/test-setup.ts:16 [EXTRACTED]
  ```
  if (!process.env.AI_ENDPOINT) {
  ```
- `process.env.AI_MODEL` ← scripts/test-setup.ts:23 [EXTRACTED]
  ```
  model: process.env.AI_MODEL || "gpt-5-mini",
  ```
- `process.env.VALIDATION_CONCURRENCY` ← scripts/validate-examples-parallel.ts:38 [EXTRACTED]
  ```
  const value = process.env.VALIDATION_CONCURRENCY;
  ```
- `process.env.VALIDATION_RETRIES` ← scripts/validation-common.ts:69 [EXTRACTED]
  ```
  const value = process.env.VALIDATION_RETRIES;
  ```
- `process.env.AI_MODEL` ← 01-introduction/code/01-hello-world.ts:15 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 01-introduction/code/01-hello-world.ts:16 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 01-introduction/code/01-hello-world.ts:17 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 01-introduction/code/02-message-types.ts:18 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 01-introduction/code/02-message-types.ts:19 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 01-introduction/code/02-message-types.ts:20 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_ENDPOINT` ← 01-introduction/code/03-model-comparison.ts:26 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 01-introduction/code/03-model-comparison.ts:27 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 01-introduction/samples/qa-program.ts:13 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 01-introduction/samples/qa-program.ts:14 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 01-introduction/samples/qa-program.ts:15 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_ENDPOINT` ← 01-introduction/solution/model-performance.ts:28 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 01-introduction/solution/model-performance.ts:29 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 01-introduction/solution/personality-test.ts:13 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 01-introduction/solution/personality-test.ts:14 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 01-introduction/solution/personality-test.ts:15 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/code/01-multi-turn.ts:18 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/code/01-multi-turn.ts:19 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/code/01-multi-turn.ts:20 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/code/02-streaming.ts:17 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/code/02-streaming.ts:18 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/code/02-streaming.ts:19 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/code/03-parameters.ts:14 [EXTRACTED]
  ```
  console.log(`🌡️  Temperature Comparison for ${process.env.AI_MODEL}\n`);
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/code/03-parameters.ts:28 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/code/03-parameters.ts:29 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.OPENAI_API_KEY` ← 02-chat-models/code/04-init-chat-model.ts:36 [EXTRACTED]
  ```
  apiKey: process.env.OPENAI_API_KEY,
  ```
- `process.env.ANTHROPIC_API_KEY` ← 02-chat-models/code/04-init-chat-model.ts:60 [EXTRACTED]
  ```
  apiKey: process.env.ANTHROPIC_API_KEY,
  ```
- `process.env.GOOGLE_API_KEY` ← 02-chat-models/code/04-init-chat-model.ts:64 [EXTRACTED]
  ```
  apiKey: process.env.GOOGLE_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/code/04-init-chat-model.ts:78 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/code/04-init-chat-model.ts:79 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/code/04-init-chat-model.ts:80 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/code/05-error-handling.ts:21 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/code/05-error-handling.ts:22 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/code/05-error-handling.ts:23 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/code/06-token-tracking.ts:15 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/code/06-token-tracking.ts:16 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/code/06-token-tracking.ts:17 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/samples/robust-chat.ts:23 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/samples/robust-chat.ts:24 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/samples/robust-chat.ts:25 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_API_KEY_BACKUP` ← 02-chat-models/samples/robust-chat.ts:72 [EXTRACTED]
  ```
  process.env.AI_API_KEY_BACKUP = process.env.AI_API_KEY;
  ```
- `process.env.AI_MODEL` ← 02-chat-models/samples/streaming-chat.ts:11 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/samples/streaming-chat.ts:12 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/samples/streaming-chat.ts:13 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/samples/token-tracker.ts:160 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/samples/token-tracker.ts:161 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/samples/token-tracker.ts:162 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/solution/chatbot.ts:12 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/solution/chatbot.ts:13 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/solution/chatbot.ts:14 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 02-chat-models/solution/temperature-lab.ts:24 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 02-chat-models/solution/temperature-lab.ts:26 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 02-chat-models/solution/temperature-lab.ts:27 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/01-messages-vs-templates.ts:20 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/01-messages-vs-templates.ts:21 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/01-messages-vs-templates.ts:22 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/02-message-construction.ts:24 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/02-message-construction.ts:25 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/02-message-construction.ts:26 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/03-basic-template.ts:18 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/03-basic-template.ts:19 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/03-basic-template.ts:20 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/04-template-formats.ts:19 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/04-template-formats.ts:20 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/04-template-formats.ts:21 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/05-few-shot.ts:18 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/05-few-shot.ts:19 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/05-few-shot.ts:20 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/06-composition.ts:18 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/06-composition.ts:19 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/06-composition.ts:20 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/07-structured-output.ts:18 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/07-structured-output.ts:19 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/07-structured-output.ts:20 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/code/08-zod-schemas.ts:19 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/code/08-zod-schemas.ts:20 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/code/08-zod-schemas.ts:21 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/samples/email-generator.ts:12 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/samples/email-generator.ts:13 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/samples/email-generator.ts:14 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/samples/prompt-builder.ts:12 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/samples/prompt-builder.ts:13 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/samples/prompt-builder.ts:14 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/samples/template-library.ts:13 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/samples/template-library.ts:14 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/samples/template-library.ts:15 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/samples/translator.ts:14 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/samples/translator.ts:15 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/samples/translator.ts:16 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/solution/format-teacher.ts:11 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/solution/format-teacher.ts:12 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/solution/format-teacher.ts:13 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 03-prompts-messages-outputs/solution/product-extractor.ts:15 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 03-prompts-messages-outputs/solution/product-extractor.ts:16 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 03-prompts-messages-outputs/solution/product-extractor.ts:17 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 04-function-calling-tools/code/02-tool-calling.ts:38 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 04-function-calling-tools/code/02-tool-calling.ts:39 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 04-function-calling-tools/code/02-tool-calling.ts:40 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 04-function-calling-tools/code/03-tool-execution.ts:37 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 04-function-calling-tools/code/03-tool-execution.ts:38 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 04-function-calling-tools/code/03-tool-execution.ts:39 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 04-function-calling-tools/code/04-multiple-tools.ts:60 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 04-function-calling-tools/code/04-multiple-tools.ts:61 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 04-function-calling-tools/code/04-multiple-tools.ts:62 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 04-function-calling-tools/solution/travel-assistant.ts:150 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 04-function-calling-tools/solution/travel-assistant.ts:151 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 04-function-calling-tools/solution/travel-assistant.ts:152 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 04-function-calling-tools/solution/weather-tool.ts:60 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 04-function-calling-tools/solution/weather-tool.ts:61 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 04-function-calling-tools/solution/weather-tool.ts:62 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/code/01-create-agent-basic.ts:45 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/code/01-create-agent-basic.ts:46 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/code/01-create-agent-basic.ts:47 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/code/02-create-agent-multi-tool.ts:97 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/code/02-create-agent-multi-tool.ts:98 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/code/02-create-agent-multi-tool.ts:99 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/code/03-agent-with-middleware.ts:62 [EXTRACTED]
  ```
  model: process.env.AI_MODEL, // e.g., gpt-5-mini
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/code/03-agent-with-middleware.ts:63 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/code/03-agent-with-middleware.ts:64 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/code/04-builtin-middleware.ts:59 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/code/04-builtin-middleware.ts:60 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/code/04-builtin-middleware.ts:61 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/samples/basic-agent-manual-loop.ts:41 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/samples/basic-agent-manual-loop.ts:42 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/samples/basic-agent-manual-loop.ts:43 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/samples/multi-tool-agent-manual.ts:61 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/samples/multi-tool-agent-manual.ts:62 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/samples/multi-tool-agent-manual.ts:63 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/solution/planning-agent.ts:147 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/solution/planning-agent.ts:148 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/solution/planning-agent.ts:149 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 05-agents/solution/research-agent.ts:83 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 05-agents/solution/research-agent.ts:84 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 05-agents/solution/research-agent.ts:85 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.MCP_SERVER_URL` ← 06-mcp/code/01-mcp-integration.ts:34 [EXTRACTED]
  ```
  const MCP_SERVER_URL = process.env.MCP_SERVER_URL || "https://mcp.context7.com/mcp";
  ```
- `process.env.CONTEXT7_API_KEY` ← 06-mcp/code/01-mcp-integration.ts:45 [EXTRACTED]
  ```
  //   "Authorization": `Bearer ${process.env.CONTEXT7_API_KEY}`
  ```
- `process.env.AI_MODEL` ← 06-mcp/code/01-mcp-integration.ts:63 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/code/01-mcp-integration.ts:64 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/code/01-mcp-integration.ts:65 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 06-mcp/code/02-mcp-stdio-local.ts:49 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/code/02-mcp-stdio-local.ts:50 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/code/02-mcp-stdio-local.ts:51 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY
  ```
- `process.env.AI_MODEL` ← 06-mcp/code/04-mcp-error-handling.ts:89 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/code/04-mcp-error-handling.ts:90 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/code/04-mcp-error-handling.ts:91 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY
  ```
- `process.env.AI_MODEL` ← 06-mcp/solution/context7-basic.ts:45 [EXTRACTED]
  ```
  model: process.env.AI_MODEL || "gpt-4o-mini",
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/solution/context7-basic.ts:46 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/solution/context7-basic.ts:47 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 06-mcp/solution/multi-server-integration.ts:77 [EXTRACTED]
  ```
  model: process.env.AI_MODEL || "gpt-4o-mini",
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/solution/multi-server-integration.ts:78 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/solution/multi-server-integration.ts:79 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 06-mcp/solution/multi-tool-agent.ts:78 [EXTRACTED]
  ```
  model: process.env.AI_MODEL || "gpt-4o-mini",
  ```
- `process.env.AI_ENDPOINT` ← 06-mcp/solution/multi-tool-agent.ts:79 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 06-mcp/solution/multi-tool-agent.ts:80 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/code/05-basic-embeddings.ts:24 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/code/05-basic-embeddings.ts:25 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/code/05-basic-embeddings.ts:26 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/code/06-vector-store.ts:19 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/code/06-vector-store.ts:20 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/code/06-vector-store.ts:21 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/code/07-similarity-scores.ts:19 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/code/07-similarity-scores.ts:20 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/code/07-similarity-scores.ts:21 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/code/08-batch-embeddings.ts:17 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/code/08-batch-embeddings.ts:18 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/code/08-batch-embeddings.ts:19 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/code/09-embedding-relationships.ts:43 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/code/09-embedding-relationships.ts:44 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/code/09-embedding-relationships.ts:45 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/samples/embedding-visualizer.ts:74 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/samples/embedding-visualizer.ts:75 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/samples/embedding-visualizer.ts:76 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/samples/multilingual-search.ts:29 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/samples/multilingual-search.ts:30 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/samples/multilingual-search.ts:31 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/samples/search-comparison.ts:44 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/samples/search-comparison.ts:45 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/samples/search-comparison.ts:46 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/solution/book-search.ts:53 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/solution/book-search.ts:54 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/solution/book-search.ts:55 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 07-documents-embeddings-semantic-search/solution/similarity-explorer.ts:36 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 07-documents-embeddings-semantic-search/solution/similarity-explorer.ts:37 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 07-documents-embeddings-semantic-search/solution/similarity-explorer.ts:38 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/code/01-when-to-use-rag.ts:28 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/code/01-when-to-use-rag.ts:29 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/code/01-when-to-use-rag.ts:30 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/code/01-when-to-use-rag.ts:148 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/code/01a-traditional-rag.ts:35 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/code/01a-traditional-rag.ts:36 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/code/01a-traditional-rag.ts:37 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/code/01a-traditional-rag.ts:41 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/code/02-agentic-rag.ts:27 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/code/02-agentic-rag.ts:28 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/code/02-agentic-rag.ts:29 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/code/02-agentic-rag.ts:33 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/samples/citation-rag.ts:76 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/samples/citation-rag.ts:77 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/samples/citation-rag.ts:78 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/samples/citation-rag.ts:82 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/samples/multi-source-rag.ts:69 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/samples/multi-source-rag.ts:70 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/samples/multi-source-rag.ts:71 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/samples/multi-source-rag.ts:75 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/solution/conversational-rag.ts:51 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/solution/conversational-rag.ts:52 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/solution/conversational-rag.ts:53 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/solution/conversational-rag.ts:57 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_EMBEDDING_MODEL` ← 08-agentic-rag-systems/solution/knowledge-base-rag.ts:60 [EXTRACTED]
  ```
  model: process.env.AI_EMBEDDING_MODEL || "text-embedding-3-small",
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/solution/knowledge-base-rag.ts:61 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/solution/knowledge-base-rag.ts:62 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/solution/knowledge-base-rag.ts:66 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_MODEL` ← 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-agent.ts:35 [EXTRACTED]
  ```
  model: process.env.AI_MODEL,
  ```
- `process.env.AI_ENDPOINT` ← 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-agent.ts:36 [EXTRACTED]
  ```
  configuration: { baseURL: process.env.AI_ENDPOINT },
  ```
- `process.env.AI_API_KEY` ← 08-agentic-rag-systems/samples/mcp-rag-server/mcp-rag-agent.ts:37 [EXTRACTED]
  ```
  apiKey: process.env.AI_API_KEY,
  ```