\# ADR-001 - Technology Stack



\*\*Status:\*\* Accepted



\*\*Date:\*\* 2026-06-30



\---



\# Context



NeverLate is a cross-platform mobile application that must support Android and iOS while minimizing development effort, maintenance costs, and time to market.



The application requires:



\- User authentication

\- Cloud database

\- Document storage

\- Push notifications

\- Analytics

\- Scalability

\- Fast MVP delivery



\---



\# Decision



The project will use the following technology stack:



| Layer | Technology |

|--------|------------|

| Mobile | Flutter |

| Backend | Firebase (Initial MVP) |

| Authentication | Firebase Authentication |

| Database | Cloud Firestore |

| Document Storage | Firebase Storage |

| Push Notifications | Firebase Cloud Messaging |

| Analytics | Firebase Analytics |

| Source Control | GitHub |

| UX/UI | Figma |



\---



\# Rationale



Flutter provides:



\- Single codebase

\- Native Android support

\- Native iOS support

\- Excellent community support

\- Reduced development costs



Firebase provides:



\- Serverless architecture

\- Fast MVP implementation

\- Authentication

\- Cloud database

\- Storage

\- Push notifications

\- Analytics



Together they allow rapid product validation without managing infrastructure.



\---



\# Consequences



\## Advantages



\- Faster development

\- Lower infrastructure costs

\- Cross-platform support

\- Easy scalability

\- Managed cloud services



\## Disadvantages



\- Vendor lock-in with Firebase

\- Future migration may be required for enterprise deployments



\---



\# Future Considerations



If NeverLate evolves into a large SaaS platform, the backend may migrate to:



\- Azure

\- AWS

\- Google Cloud

\- Kubernetes

\- PostgreSQL

\- Microservices architecture

