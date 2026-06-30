\# NeverLate - Engineering Standards



\## Purpose



Define the engineering standards for the NeverLate MVP.



\---



\## Mobile Framework



NeverLate will use Flutter to build Android and iOS applications from a single codebase.



\---



\## Flutter Architecture



The project will use a simple Feature-First architecture with Clean Architecture principles.



Main structure:



```text

lib/

├── core/

├── features/

├── shared/

└── main.dart



\### State Management



NeverLate will use Riverpod for state management.



Reasons:



Clean dependency injection

Good scalability

Strong Flutter support

Test-friendly structure



\### Backend Platform



The MVP will use Firebase.



Firebase services:



Firebase Authentication

Cloud Firestore

Firebase Storage

Firebase Cloud Messaging

Firebase Analytics



\### Git Branching Strategy



Branches:



main

develop

feature/\*



Branch usage:



Branch	Purpose

main	Stable production-ready code

develop	Integration branch for active development

feature/\*	Individual feature work



Example branches:



feature/auth-login

feature/create-reminder

feature/document-upload



\### Commit Convention



Commit messages should be short and clear.



Examples:



Add login screen

Create reminder model

Add Firebase configuration

Fix document upload validation

Update architecture documentation



\### Code Quality Rules

Keep code readable.

Avoid large files.

Separate UI, business logic, and data access.

Reuse shared widgets.

Document important decisions.

Avoid hardcoded values when possible.



\### MVP Engineering Principle



The MVP should be:



Simple, professional, and maintainable.



The goal is not to over-engineer the first version, but to create a clean foundation that can grow.

