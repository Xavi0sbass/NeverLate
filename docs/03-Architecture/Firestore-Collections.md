\# NeverLate - Firestore Collections Design



\## Purpose

Define the initial Firestore collections required for the NeverLate MVP.



\---



\## Collections



\### 1. users



Stores user profile information.



Path:



```text

users/{userId}



\### 2. reminders



Stores reminder records.



Path:



reminders/{reminderId}



Fields:



userId

title

description

category

eventDate

reminderDate

location

priority

status

createdAt

updatedAt



Status values:



pending

completed

overdue

cancelled



\### 3. checklistItems



Stores required items for each reminder.



Path:



checklistItems/{checklistItemId}



Fields:



userId

reminderId

itemName

isCompleted

createdAt

updatedAt



\### 4. documents



Stores document metadata.



Path:



documents/{documentId}



Fields:



userId

reminderId

fileName

fileType

filePath

fileUrl

uploadedAt



\### 5. notificationSettings



Stores notification preferences.



Path:



notificationSettings/{settingId}



Fields:



userId

reminderId

notifyBeforeMinutes

isEnabled

createdAt

updatedAt

Storage Path



Uploaded files should be stored in Firebase Storage using this structure:



documents/{userId}/{reminderId}/{fileName}

Query Strategy



Common queries:



Get all reminders for user:

reminders where userId == currentUserId



Get pending reminders:

reminders where userId == currentUserId and status == pending



Get reminder checklist:

checklistItems where reminderId == selectedReminderId



Get reminder documents:

documents where reminderId == selectedReminderId

Design Notes

Every collection must include userId when the data belongs to a user.

Firestore security rules must validate ownership using userId.

Documents should not be publicly accessible.

Reminder status should be updated when the user completes or cancels a reminder.

Overdue status may be calculated by the app or backend in a future version.





