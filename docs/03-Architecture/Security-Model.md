\# NeverLate - Physical Architecture



\## Purpose

Define how the NeverLate MVP components will be physically implemented using Flutter and Firebase.



\---



\## Physical Architecture Diagram



```mermaid

flowchart TD

&#x20;   User\[Mobile User]



&#x20;   User --> App\[Flutter App]



&#x20;   App --> Auth\[Firebase Authentication]

&#x20;   App --> Firestore\[Cloud Firestore]

&#x20;   App --> Storage\[Firebase Storage]

&#x20;   App --> FCM\[Firebase Cloud Messaging]

&#x20;   App --> Analytics\[Firebase Analytics]



&#x20;   Firestore --> Reminders\[(Reminders Collection)]

&#x20;   Firestore --> Users\[(Users Collection)]

&#x20;   Firestore --> Checklists\[(Checklist Items)]

&#x20;   Firestore --> Notifications\[(Notification Settings)]



&#x20;   Storage --> Docs\[(User Documents)]



&#x20;   FCM --> Device\[Android / iOS Device]

```



\---



\## Component Mapping



| Component | Technology |

|---|---|

| Mobile App | Flutter |

| Authentication | Firebase Authentication |

| Database | Cloud Firestore |

| Document Storage | Firebase Storage |

| Push Notifications | Firebase Cloud Messaging |

| Analytics | Firebase Analytics |

| Source Control | GitHub |

| UX/UI Design | Figma |



\---



\## Main Data Flow



1\. User opens the Flutter app.

2\. User authenticates using Firebase Authentication.

3\. App reads and writes reminder data in Cloud Firestore.

4\. App uploads documents to Firebase Storage.

5\. App stores document metadata in Cloud Firestore.

6\. App receives push notifications using Firebase Cloud Messaging.

7\. App sends usage events to Firebase Analytics.



\---



\## Security Notes



\- Each user must only access their own reminders.

\- Documents must be stored under a user-specific path.

\- Firestore security rules must restrict access by authenticated user ID.

\- Firebase Storage rules must restrict file access by authenticated user ID.

\- Sensitive data should not be stored in plain text unless required for MVP validation.



\---



\## MVP Deployment Model



```text

Developer Machine

&#x20;     |

&#x20;     | Flutter Build

&#x20;     |

Android APK / AAB        iOS Build

&#x20;     |                    |

Google Play Console      Apple App Store Connect

&#x20;     |                    |

Android Users            iOS Users

```



Document Storage Security



Documents must be stored in a user-specific path.



Example:



documents/{userId}/{fileName}



Storage rules must validate that:



The user is authenticated.

The user ID in the storage path matches the authenticated user ID.

Users cannot access documents from other users.

Firestore Security Rules Direction



Firestore rules must validate:



User is authenticated.

Requesting user ID matches the document owner.

Users cannot read or modify other users' data.



Example concept:



request.auth.uid == resource.data.userId

Sensitive Data



The MVP may store sensitive personal data such as:



Medical appointment information

Medical exam documents

Vehicle documents

Bills and receipts



Security considerations:



Do not expose files publicly.

Avoid storing unnecessary sensitive data.

Use secure backend services.

Apply privacy policy before production release.

Audit and Monitoring



Initial MVP audit considerations:



Track user login events.

Track document upload events.

Track reminder creation events.

Track completed reminders.

Monitor failed authentication attempts.

Future Security Enhancements



Future versions may include:



Multi-factor authentication

Biometric login

Data encryption improvements

Role-based access control

Family sharing permissions

Admin portal security

Compliance review



