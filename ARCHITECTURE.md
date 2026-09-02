# ARCHITECTURE

## 1. Frontend Layer (Next.js + TypeScript)
- Hosts role-specific interfaces for Patient, Doctor, Hospital Staff, Emergency Personnel, and Admin.
- Handles workflow screens: profile, consent, emergency access request, audit views.
- Uses reusable UI from `components/`.

## 2. Backend/Application Layer (Next.js API)
- Provides API endpoints for app workflows.
- Coordinates database access, encryption utilities, IPFS upload/download, blockchain logging, and AI service calls.
- Enforces authorization checks before sensitive actions.

## 3. Database Layer (Supabase PostgreSQL)
- Stores users, role mappings, patient profiles, record metadata, consent states, and operational logs.
- Uses Supabase Auth for identity and Row Level Security for data isolation.

## 4. AI Service Layer (Python FastAPI)
- Exposes APIs for:
  - Identity matching from partial patient data
  - Emergency risk priority scoring
- Operates as decision support only.

## 5. Blockchain Layer (Solidity + Hardhat)
- Stores immutable events only:
  - Consent events
  - Audit events
  - Emergency override events
  - IPFS references/hashes
- Never stores raw medical files.

## 6. Storage Layer (IPFS)
- Stores encrypted medical files (e.g., MRI/X-ray reports).
- Returns content-addressed hashes used as references in database/blockchain logs.

## 7. Encryption Layer
- AES encryption performed before file upload to IPFS.
- Decryption allowed only for authorized emergency/clinical workflows.

## 8. Communication Flow (High-level)
1. User action initiated in frontend.
2. Next.js API validates role/permissions.
3. Sensitive files encrypted and uploaded to IPFS.
4. Metadata and permissions persisted in Supabase.
5. Audit/consent/emergency event written to blockchain.
6. Optional AI service calls return matching/risk-support outputs.
7. Result returned to frontend with full traceability.

## 9. Responsibility Boundaries
- Frontend: user interaction and presentation.
- App backend: policy enforcement and orchestration.
- Database: state and permissions.
- AI service: scoring/matching assistance.
- Blockchain: tamper-evident audit proofs.
- IPFS: encrypted file distribution/storage.
