\# NeverLate - Checklist Engine Design



\## Purpose

Define how NeverLate will manage the "What do I need to bring?" feature.



\---



\## Feature Objective



The Checklist Engine helps users prepare for an event by showing required items, documents, or actions before the event date.



Examples:

\- What documents should I bring to a medical appointment?

\- What do I need for vehicle inspection?

\- What information do I need to pay a bill?



\---



\## Checklist Types



\### 1. Manual Checklist



The user manually adds required items.



Example:



```text

\- ID card

\- Appointment confirmation

\- Previous medical exams



\### 2. Template-Based Checklist



The app suggests default checklist items based on the reminder category.



Example: Vehicle Inspection



\- Driver license

\- Vehicle registration

\- Insurance

\- Inspection appointment confirmation



\### Initial Checklist Templates



Medical Appointment



\- ID card

\- Insurance card

\- Appointment confirmation

\- Previous medical results

\- Medication list



Medical Exam



\- ID card

\- Medical order

\- Fasting instructions

\- Previous medical results



Bill Payment



\- Account number

\- Previous bill

\- Payment method



Vehicle Inspection

\- Driver license

\- Vehicle registration

\- Insurance

\- Appointment confirmation



Vehicle Maintenance

\- Vehicle registration

\- Maintenance history

\- Warranty information



\### Data Model



Collection:



checklistItems/{checklistItemId}



Fields:



checklistItemId

userId

reminderId

itemName

isCompleted

source

createdAt

updatedAt



Source values:



manual

template



\### Design Notes

Each reminder can have multiple checklist items.

Checklist items can be manually added or generated from a template.

Users must be able to mark checklist items as completed.

Future versions may use AI to suggest required items.

