# Sync Solutions — Legal & Compliance Rules (rule.md)

Read this before implementing any feature involving user accounts, events, availability, or personal data.

---

## PDPA (Personal Data Protection Act)

### What it is
Thailand's personal data protection law governing the collection, use, disclosure, and storage of personal data.

### What it requires
- Lawful basis for processing
- Purpose limitation
- Data minimization
- Transparency
- Security
- Data subject rights
- Retention & deletion

### Rules for AI agents
- If the system collects personal data (name, phone, email), it must collect only the minimum needed for scheduling and inviting.
- If the system processes personal data, it must have a documented lawful basis (e.g. consent, or necessity to perform the scheduling service the user signed up for).
- If consent is the lawful basis, the system must obtain consent before processing and must allow users to withdraw consent where legally applicable.
- If the system lets users manually enter availability or location instead of syncing external calendars or contacts, it must store only what the user entered and must not infer or collect additional personal data.
- If the system shares one member's availability or contact information with other members of a group, it must limit the information to what is necessary for scheduling (for example, showing "Busy" instead of event details).
- Personal data must only be visible to authorized users with a legitimate need to access it.
- If the system stores personal data, it must protect it from unauthorized access, modification, disclosure, or loss using appropriate security controls (such as encryption in transit and access controls).
- If users request correction or deletion of their personal data, the system must support those requests where legally applicable.
- Sensitive personal data (health, religion, biometric data, etc.) must not be collected unless explicitly required for the feature and legally permitted.
- Personal data must not be used for purposes unrelated to the original purpose (such as marketing) without an appropriate lawful basis.
- Personal data must not be retained longer than necessary. Deleted accounts or obsolete records should have their personal data securely deleted or anonymized where legally permitted.

---

## Computer Crime Act §26

### What it is
Requires certain service providers to retain applicable computer traffic data for lawful investigations.

### What it requires
- Retain required traffic data
- Protect log integrity
- Restrict log access

### Rules for AI agents
- If the system authenticates users, it must generate logs sufficient to identify account activity (account ID, timestamp, IP address where applicable).
- If important account or event actions occur (creating, editing, cancelling an event, confirming attendance, changing permissions), the system should create audit logs tied to the authenticated account.
- Passwords, authentication tokens, API keys, session secrets, and similar credentials must never be stored in logs or in plaintext.
- Log data must be protected against unauthorized modification or deletion.
- Access to logs must be restricted to authorized administrators or services only.
- Log retention must follow applicable legal and organizational retention requirements.

---

## Electronic Transactions Act (§9, §26, §28)

### What it is
Recognizes electronic records and electronic signatures under Thai law.

### What it requires
- Electronic intent
- Identity of signer
- Reliable electronic signatures where legally required

### Rules for AI agents
- If the system requires users to accept the Terms of Service or Privacy Policy, it must record the acceptance event.
- Each acceptance record must include the user identifier, timestamp, and the version of the document accepted.
- If the Terms of Service or Privacy Policy is updated, acceptance of the new version must be recorded as a separate record rather than overwriting the previous acceptance.
- Availability selections or attendance confirmations should be treated as normal application actions unless the feature is explicitly intended to create legal obligations.
- If a confirmation action is generated automatically by the system (for example, auto-confirming after no response), it must be distinguishable from a confirmation explicitly made by the user.
- Electronic records and acceptance records must be protected against unauthorized alteration to preserve their integrity and reliability.