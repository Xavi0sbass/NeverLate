\# NeverLate - Initial Data Model



\## Purpose

Define the initial data entities required for the NeverLate MVP.



\## Entities



\### 1. Users

Stores basic user profile information.



Fields:

\- userId

\- fullName

\- email

\- phoneNumber

\- createdAt

\- updatedAt



\### 2. Reminders

Stores the main reminder information.



Fields:

\- reminderId

\- userId

\- title

\- description

\- categoryId

\- eventDate

\- reminderDate

\- location

\- priority

\- status

\- createdAt

\- updatedAt



\### 3. Categories

Stores reminder categories.



Fields:

\- categoryId

\- name

\- description

\- icon



Initial categories:

\- Medical Appointment

\- Medical Exam

\- Bill Payment

\- Vehicle Inspection

\- Vehicle Maintenance

\- Personal Errand

\- Custom Reminder



\### 4. Documents

Stores document metadata.



Fields:

\- documentId

\- userId

\- reminderId

\- fileName

\- fileType

\- fileUrl

\- uploadedAt



\### 5. ChecklistItems

Stores required items for each reminder.



Fields:

\- checklistItemId

\- reminderId

\- itemName

\- isCompleted

\- createdAt



\### 6. Notifications

Stores notification configuration and history.



Fields:

\- notificationId

\- reminderId

\- userId

\- notificationDate

\- status

\- sentAt



\## Relationships



```text

User 1 ─── \* Reminders

Reminder 1 ─── \* Documents

Reminder 1 ─── \* ChecklistItems

Reminder 1 ─── \* Notifications

Category 1 ─── \* Reminders

