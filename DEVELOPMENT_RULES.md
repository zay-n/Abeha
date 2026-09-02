# DEVELOPMENT RULES

## 1. Coding Conventions
- Prefer TypeScript for app/backend code.
- Keep modules small and focused.
- Use clear naming for healthcare workflow entities.
- Reuse shared utilities/components before adding duplicates.

## 2. Git Branching Strategy
- Main branch is protected.
- Use short-lived feature branches per issue.
- Branch naming convention: `feature/<issue-or-scope>` or `fix/<issue-or-scope>`.

## 3. Pull Request Expectations
- One focused concern per PR.
- Explain what changed, why, and test evidence.
- Include security impact notes for sensitive workflows.

## 4. Testing Requirements
- Add/maintain unit tests for changed logic.
- Add integration tests for critical workflows when available.
- Validate auth, consent, and emergency-access paths.

## 5. Security Rules
- Never commit `.env`, secrets, private keys, or production credentials.
- Use synthetic data only.
- Encrypt medical files before IPFS upload.
- Never store raw medical files on blockchain.
- Enforce role checks and least privilege.

## 6. Dependency Rules
- Prefer existing dependencies.
- Add new dependency only with clear need and security review.
- Keep dependency updates minimal and documented.

## 7. Definition of Done
A task is done when:
- Requirements are implemented within scope.
- Relevant tests pass.
- Security constraints are satisfied.
- Documentation is updated for behavior changes.
- PR description clearly explains verification steps.
