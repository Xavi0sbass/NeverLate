\# NeverLate - MVP Use Cases



\## UC-01 - Register User



Actor:

\- User



Description:

The user creates a new account in NeverLate.



Basic Flow:

1\. User opens the app.

2\. User selects Register.

3\. User enters name, email, and password.

4\. System creates the account.

5\. User is redirected to Home Dashboard.



\---



\## UC-02 - Create Reminder



Actor:

\- User



Description:

The user creates a reminder for an important event.



Basic Flow:

1\. User selects Add Reminder.

2\. User enters title, category, date, time, and notes.

3\. User optionally adds location.

4\. User saves the reminder.

5\. System stores the reminder.



\---



\## UC-03 - Attach Document



Actor:

\- User



Description:

The user attaches a document or image to a reminder.



Basic Flow:

1\. User opens a reminder.

2\. User selects Attach Document.

3\. User uploads a PDF or image.

4\. System stores the file.

5\. System links the file to the reminder.



\---



\## UC-04 - Manage Checklist



Actor:

\- User



Description:

The user manages the required items for an event.



Basic Flow:

1\. User opens a reminder.

2\. User adds required items.

3\. User marks items as completed.

4\. System saves checklist status.



\---



\## UC-05 - Receive Notification



Actor:

\- User



Description:

The user receives a mobile notification before the event.



Basic Flow:

1\. Reminder date approaches.

2\. System checks notification schedule.

3\. System sends push notification.

4\. User opens the reminder.



\---



\## UC-06 - Complete Reminder



Actor:

\- User



Description:

The user marks a reminder as completed.



Basic Flow:

1\. User opens reminder details.

2\. User selects Complete.

3\. System updates reminder status.

4\. System updates statistics.

