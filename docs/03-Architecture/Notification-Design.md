\# NeverLate - Notification Design



\## Purpose

Define how NeverLate will notify users about upcoming reminders.



\---



\## Notification Objective



NeverLate must notify users before important events such as:



\- Medical appointments

\- Medical exams

\- Bill payments

\- Vehicle inspections

\- Vehicle maintenance

\- Personal errands

\- Custom reminders



\---



\## Notification Technology



The MVP will use:



\- Firebase Cloud Messaging

\- Local mobile notifications



\---



\## Notification Types



\### 1. Push Notifications



Used when the app needs to notify the user from the backend or cloud service.



Examples:

\- Reminder coming soon

\- Payment due soon

\- Vehicle inspection due soon



\### 2. Local Notifications



Used when the app schedules a notification directly on the mobile device.



Examples:

\- 1 day before appointment

\- 1 hour before appointment

\- Same-day reminder



\---



\## Default Reminder Times



Initial default options:



\- 1 week before

\- 1 day before

\- 1 hour before

\- At event time



\---



\## Notification Message Examples



\### Medical Appointment



```text

NeverLate Reminder: You have a medical appointment tomorrow. Check what you need to bring.



\### Bill Payment

NeverLate Reminder: Your bill payment is due soon.



\### Vehicle Inspection

NeverLate Reminder: Your vehicle inspection is coming up. Review required documents.



\### Notification Data



Each notification should include:



notificationId

userId

reminderId

notificationDate

notificationType

status

sentAt

createdAt

updatedAt



\### Notification Status Values

scheduled

sent

failed

cancelled



\### Design Notes

Users should be able to enable or disable notifications.

Users should be able to choose reminder times.

Notifications must link back to the reminder details screen.

Future versions may support recurring reminders and email notifications.



