\# NeverLate - Architecture Diagram



\## High-Level Architecture



```mermaid

flowchart TD

&#x20;   User\[User] --> MobileApp\[Flutter Mobile App]



&#x20;   MobileApp --> Auth\[Authentication Service]

&#x20;   MobileApp --> API\[Backend API]

&#x20;   MobileApp --> Push\[Push Notification Service]



&#x20;   API --> DB\[(Database)]

&#x20;   API --> Storage\[(Document Storage)]

&#x20;   API --> Analytics\[Analytics Engine]

&#x20;   API --> Checklist\[Checklist Engine]

&#x20;   API --> Reminder\[Reminder Engine]



&#x20;   Reminder --> Push

&#x20;   Checklist --> DB

&#x20;   Analytics --> DB

&#x20;   Storage --> DB



Component Description

Flutter Mobile App



Cross-platform mobile application for Android and iOS.



Authentication Service



Handles user registration, login, and identity validation.



Backend API



Central layer for business logic and communication between the mobile app and backend services.



Database



Stores users, reminders, categories, checklist items, notification settings, and statistics.



Document Storage



Stores uploaded files such as PDFs, images, receipts, medical documents, and vehicle documents.



Push Notification Service



Sends reminders to the user's mobile device.



Analytics Engine



Processes basic statistics such as completed, pending, and overdue reminders.



Checklist Engine



Manages the required items for each reminder.



Reminder Engine



Manages event dates, reminder schedules, and reminder status.

