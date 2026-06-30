\# NeverLate - User Flow



\## Purpose



Define the primary user journey through the NeverLate MVP.



\---



\## Main User Flow



```mermaid

flowchart TD



A\[Open App]



A --> B{Authenticated?}



B -- No --> C\[Login / Register]



C --> D\[Home Dashboard]



B -- Yes --> D



D --> E\[Create Reminder]



E --> F\[Select Category]



F --> G\[Enter Reminder Details]



G --> H\[Attach Documents]



H --> I\[Add Checklist Items]



I --> J\[Save Reminder]



J --> K\[Reminder Stored]



K --> L\[Notification Scheduled]



L --> M\[Reminder Appears on Calendar]



M --> N\[Notification Received]



N --> O\[Open Reminder]



O --> P\[Review Documents]



P --> Q\[Review Checklist]



Q --> R\[Complete Reminder]



R --> S\[Statistics Updated]

```



\---



\## Happy Path



1\. User logs in.

2\. User creates a reminder.

3\. User uploads documents.

4\. User creates a checklist.

5\. Reminder is saved.

6\. Notification is scheduled.

7\. User receives notification.

8\. User reviews required items.

9\. User completes the reminder.

10\. Statistics are updated.



\---



\## Future User Flows



\- Family shared reminders

\- Recurring reminders

\- AI-generated checklist

\- Calendar synchronization

\- Voice reminders

\- Smart suggestions

