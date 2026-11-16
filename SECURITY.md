# Security Policy

This project is in engineering planning. These controls are requirements, not a claim that an implementation has been deployed or audited.

Do not publish credentials, exploit details affecting a live deployment, or private operational data in public issues. Report security concerns privately to the repository owner with affected component, impact, and reproduction evidence.

Minimum requirements: TLS; unique device credentials and rotation/revocation; restricted database network access; SSH key authentication; secrets outside version control; API validation and authorization; audit logs; encrypted backups and restore tests; dependency/container review. Never expose the Raspberry Pi local database directly to the public internet.
