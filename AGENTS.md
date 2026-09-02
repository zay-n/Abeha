# AGENTS.md

Guidelines for AI coding agents working in this repository:

1. Do not over-engineer. Build only what is needed for the current issue.
2. Follow the agreed ABEHA architecture and MVP scope.
3. Do not modify unrelated modules or files.
4. Protect secrets: never commit keys, tokens, credentials, or `.env` files.
5. Use synthetic/mock data only. Never use real patient or Aadhaar data.
6. Add or update tests for changed behavior when test infrastructure exists.
7. Validate your changes before finalizing.
8. Explain proposed changes before major architectural modifications.
