# PRODUCT SPEC

## 1. Users
- Patient
- Doctor
- Hospital Staff
- Emergency Personnel
- Administrator

## 2. User Permissions (Initial)
- **Patient**: manage consent, view own records and access logs.
- **Doctor**: view/update records when authorized.
- **Hospital Staff**: manage intake and transfer records.
- **Emergency Personnel**: request emergency override access with justification.
- **Administrator**: configure roles, policies, and audit oversight.

## 3. Core Workflows
1. Authentication and role-based sign-in
2. Patient profile creation and maintenance
3. Medical record upload, encryption, and retrieval
4. Consent grant/revoke lifecycle
5. Emergency override request and validation
6. Audit review of all sensitive actions

## 4. Medical Record Lifecycle
1. Record created or uploaded by authorized role.
2. File encrypted using AES.
3. Encrypted file uploaded to IPFS.
4. Metadata (not raw file) stored in database.
5. IPFS hash reference and relevant event logged on blockchain.
6. Authorized retrieval decrypts content for permitted users.

## 5. Consent Workflow
1. Patient grants or revokes consent for provider/hospital access.
2. Consent state stored in database.
3. Consent change event logged to blockchain.
4. Access checks must reference current consent policy.

## 6. Emergency Override Workflow
1. Emergency Personnel initiates override request with reason.
2. System verifies role, context, and policy constraints.
3. Emergency event logged on blockchain and audit trail.
4. Time-bound access granted where applicable.
5. Emergency contact notified.

## 7. AI Functionality
- **Identity Matching**: estimates probable patient from partial details.
- **Risk Prioritization**: provides emergency priority score.
- AI outputs are advisory and require human clinical judgment.

## 8. Blockchain Functionality
- Immutable logging of consent, access, and override events.
- Proof-oriented event storage only; no raw medical file content.

## 9. IPFS Functionality
- Secure storage of encrypted medical files.
- Content hash references integrated with audit and retrieval flows.
