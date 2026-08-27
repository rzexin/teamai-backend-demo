---
title: langchainjs-for-beginners component
domain: code-knowledge
source:
  - scripts/create-model.ts
  - scripts/validation-common.ts
---

# Component

- `createChatModel` ← scripts/create-model.ts:23 [EXTRACTED]
  ```
  export function createChatModel(options?: ConstructorParameters<typeof ChatOpenAI>[0]) {
  ```
- `createEmbeddingsModel` ← scripts/create-model.ts:40 [EXTRACTED]
  ```
  export function createEmbeddingsModel(options?: ConstructorParameters<typeof OpenAIEmbeddings>[0]) {
  ```
- `INTERACTIVE_FILES` ← scripts/validation-common.ts:20 [EXTRACTED]
  ```
  export const INTERACTIVE_FILES = [
  ```
- `SERVER_FILES` ← scripts/validation-common.ts:29 [EXTRACTED]
  ```
  export const SERVER_FILES = [
  ```
- `SKIP_FILES` ← scripts/validation-common.ts:49 [EXTRACTED]
  ```
  export const SKIP_FILES = [
  ```
- `TIMEOUT_MS` ← scripts/validation-common.ts:59 [EXTRACTED]
  ```
  export const TIMEOUT_MS = 120000; // 120 seconds (2 minutes)
  ```
- `findCodeFiles` ← scripts/validation-common.ts:91 [EXTRACTED]
  ```
  export async function findCodeFiles(dir: string): Promise<string[]> {
  ```
- `getInteractiveInput` ← scripts/validation-common.ts:121 [EXTRACTED]
  ```
  export function getInteractiveInput(filePath: string): string | undefined {
  ```
- `getServerConfig` ← scripts/validation-common.ts:129 [EXTRACTED]
  ```
  export function getServerConfig(filePath: string) {
  ```
- `shouldSkipFile` ← scripts/validation-common.ts:136 [EXTRACTED]
  ```
  export function shouldSkipFile(filePath: string): boolean {
  ```
- `getSkipReason` ← scripts/validation-common.ts:143 [EXTRACTED]
  ```
  export function getSkipReason(filePath: string): string | undefined {
  ```
- `runServerExample` ← scripts/validation-common.ts:151 [EXTRACTED]
  ```
  export function runServerExample(
  ```
- `runExample` ← scripts/validation-common.ts:319 [EXTRACTED]
  ```
  export async function runExample(filePath: string): Promise<TestResult> {
  ```
- `findChapters` ← scripts/validation-common.ts:343 [EXTRACTED]
  ```
  export async function findChapters(projectRoot: string): Promise<string[]> {
  ```
- `collectAllCodeFiles` ← scripts/validation-common.ts:357 [EXTRACTED]
  ```
  export async function collectAllCodeFiles(
  ```
- `displayTestSummary` ← scripts/validation-common.ts:387 [EXTRACTED]
  ```
  export function displayTestSummary(allFiles: string[]): void {
  ```
- `displayFinalResults` ← scripts/validation-common.ts:416 [EXTRACTED]
  ```
  export function displayFinalResults(
  ```