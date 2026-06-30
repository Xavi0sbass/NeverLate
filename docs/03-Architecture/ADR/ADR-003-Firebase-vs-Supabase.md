\# ADR-003 - Firebase vs Supabase



\*\*Status:\*\* Accepted



\*\*Date:\*\* 2026-06-30



\---



\## Context



NeverLate requires a backend platform for the MVP that supports authentication, database, document storage, push notifications, analytics, and fast delivery.



\---



\## Options Considered



\### Option 1: Firebase



Pros:

\- Strong mobile app support

\- Firebase Authentication

\- Cloud Firestore

\- Firebase Storage

\- Firebase Cloud Messaging

\- Firebase Analytics

\- Good integration with Flutter

\- Fast MVP delivery



Cons:

\- Vendor lock-in

\- No traditional relational database model

\- Cost model must be monitored as usage grows



\---



\### Option 2: Supabase



Pros:

\- PostgreSQL database

\- Open-source platform

\- Authentication

\- Storage

\- Edge functions

\- SQL-based data model



Cons:

\- Push notification support requires additional services

\- Analytics may require additional tooling

\- Mobile push architecture may be less direct than Firebase



\---



\## Decision



NeverLate will use Firebase for the MVP.



\---



\## Rationale



Firebase is better aligned with the MVP because the application is mobile-first and requires authentication, storage, notifications, analytics, and fast delivery with minimal backend complexity.



\---



\## Consequences



\### Positive



\- Faster MVP implementation

\- Native mobile-friendly backend services

\- Built-in push notification support

\- Built-in analytics

\- Lower operational overhead



\### Negative



\- Firebase lock-in

\- Firestore data modeling requires careful planning

\- Future migration may be needed if the product grows into a larger SaaS platform



\---



\## Future Considerations



Supabase or a custom backend may be reconsidered if NeverLate requires:



\- Complex reporting

\- Relational data models

\- Advanced SQL queries

\- Enterprise integrations

\- Multi-tenant SaaS administration

