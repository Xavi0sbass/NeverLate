\# NeverLate - Firebase Storage Design



\## Purpose

Define how NeverLate will store user-uploaded documents and images.



\---



\## Storage Objective



Firebase Storage will be used to store files uploaded by users, such as:



\- Medical documents

\- Medical exam results

\- Vehicle documents

\- Bills and receipts

\- Personal documents

\- Images



\---



\## Storage Structure



Files should be stored using this path structure:



```text

documents/{userId}/{reminderId}/{fileName}



\### File Metadata



File metadata will be stored in Cloud Firestore, not only in Firebase Storage.



Firestore collection:



documents/{documentId}



Fields:



documentId

userId

reminderId

fileName

fileType

filePath

fileUrl

uploadedAt



\### Access Control



Users must only access their own files.



Storage rules must validate:



request.auth != null

request.auth.uid == userId



\### File Types Allowed



Initial allowed file types:



PDF

JPG

JPEG

PNG



\### File Size Limit



Recommended MVP file size limit:



10 MB per file



\### Design Notes

Files should not be publicly accessible.

File URLs should not be exposed without authentication.

Each uploaded file must be linked to a reminder.

Deleted reminders should also remove or archive related files.

Storage usage should be tracked per user in a future version.

