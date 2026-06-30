\# NeverLate - Architecture Overview



\## Architecture Goal

Design a mobile-first platform that supports reminders, document storage, checklists, notifications, calendar views, and basic statistics for Android and iOS users.



\## High-Level Architecture



```text

User

&#x20;|

&#x20;| Android / iOS App

&#x20;|

Flutter Mobile Application

&#x20;|

Backend Services

&#x20;|

Database + Document Storage + Notifications



\## Main Components



\### 1. Mobile Application



The mobile app will be built using Flutter to support both Android and iOS from a single codebase.



Main responsibilities:



User interface

Login and registration

Reminder creation

Document upload

Checklist management

Calendar view

Notification display

Basic statistics



\### 2. Authentication



Authentication will allow users to securely register and log in.



Initial options:



Email and password

Google login



\### 3. Backend Services



Backend services will manage the business logic of the application.



Main responsibilities:



User data

Reminder data

Checklist data

Document metadata

Notification scheduling

Statistics processing



\### 4. Database



The database will store structured application data.



Examples:



Users

Reminders

Categories

Checklist items

Notification settings

Statistics



\### 5. Document Storage



Document storage will be used to save uploaded files and images.



Examples:



Medical documents

Vehicle documents

Bills

Personal documents

Receipts



\### 6. Notification Service



The notification service will send reminders to the user's mobile device before the event date.



\### 7. Analytics



The analytics layer will provide basic visibility into:



Completed reminders

Pending reminders

Overdue reminders

Reminder categories

Technology Direction



Preferred approach:



Flutter for mobile development

Firebase or Supabase for backend

Firebase Cloud Messaging for push notifications

GitHub for source control

Figma for UX/UI design

Architecture Principles

Mobile-first

Secure by design

Simple MVP first

Scalable backend

Cross-platform development

Clear separation between UI, business logic, and data

