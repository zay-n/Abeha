# DEMO SCENARIO: Emergency Transfer (Hospital A -> Hospital B)

1. Patient previously has encrypted medical records at Hospital A.
2. Patient is transferred to Hospital B during an emergency and is unconscious.
3. Hospital B staff enters partial patient details available at intake.
4. AI Identity Matching Engine returns probable patient match candidates.
5. Authorized Emergency Personnel submits emergency access request with reason.
6. System validates role, emergency context, and policy constraints.
7. Emergency override event is recorded on blockchain.
8. Consent and audit checks are applied according to rules.
9. Encrypted medical record references are located.
10. Encrypted files are retrieved from IPFS using stored references.
11. Files are decrypted only for authorized emergency workflow.
12. AI emergency risk prioritization score is generated for decision support.
13. Registered emergency contact receives notification.
14. Full audit trail is persisted for review (request, decision, access, notification).
