# ABEHA

## AI-Assisted Blockchain-Enabled Emergency Healthcare Access and Consent Management Framework Using IPFS Inspired by ABDM Architecture

ABEHA is a final-year Computer Science engineering project by a two-student team. It is an **academic prototype** focused on secure, privacy-aware emergency healthcare record access.

## Problem Being Solved
In emergency transfers, receiving hospitals may lack full patient context. ABEHA demonstrates how authorized emergency teams can retrieve encrypted records quickly while preserving consent controls, traceability, and integrity.

## Project Goals
- Enable emergency access workflows with role-based controls
- Protect patient privacy with encryption and secure access rules
- Maintain auditable records of consent and emergency override events
- Demonstrate AI-assisted identity matching and emergency risk prioritization

## Major Technologies
- **Frontend & App**: Next.js, TypeScript, Tailwind CSS, shadcn/ui
- **Backend**: Next.js API routes/server features
- **Database & Auth**: Supabase, PostgreSQL, Supabase Auth, RLS
- **AI Service**: Python, FastAPI, scikit-learn, pandas, numpy
- **Blockchain**: Solidity, Hardhat, local/private EVM
- **Storage**: IPFS, Pinata (or equivalent)

## Architecture Overview
- Next.js app for user-facing workflows and API orchestration
- Supabase/PostgreSQL for identities, metadata, permissions, and consent state
- Python FastAPI service for identity matching and risk scoring
- Smart contracts for immutable audit/consent/emergency event logging
- IPFS for encrypted medical file storage; blockchain stores references only

## Major Modules
1. Authentication & role management
2. Patient digital health profile
3. Medical record management
4. AES encryption
5. IPFS medical file storage
6. Consent management
7. Blockchain audit logging
8. Emergency override access
9. AI-assisted identity matching
10. AI emergency risk prioritization
11. Emergency contact notification
12. Audit dashboard

## Current MVP Scope
- **P0**: Auth, roles, patient profile, records, AES encryption, IPFS, consent, blockchain audit, emergency override, emergency contact notification
- **P1**: AI identity matching, AI risk scoring, hospital transfer simulation, audit dashboard
- **P2**: Emergency wallet simulation, insurance simulation, advanced analytics

## Setup Instructions (Placeholder)
Detailed setup steps will be added as modules are scaffolded.

## Development Roadmap (Placeholder)
Milestones and issue-based implementation plan will be tracked as GitHub Issues.

## Security Disclaimer
- Never commit secrets, private keys, or `.env` files.
- Never store raw medical files on blockchain.
- Encrypt medical files before IPFS upload.
- Use synthetic data only.

## Academic Prototype Disclaimer
This repository is for educational prototyping only. It is not a production healthcare platform and does not provide medical diagnosis or treatment decisions.
