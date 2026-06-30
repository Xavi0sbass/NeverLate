\# NeverLate - Git Workflow



\## Purpose



Define the Git workflow for the NeverLate MVP.



\---



\## Branches



| Branch | Purpose |

|---|---|

| main | Stable production-ready code |

| develop | Integration branch for active development |

| feature/\* | Work for individual features |



\---



\## Workflow



\### 1. Start from develop



```powershell

git checkout develop

git pull



\### 2. Create a feature branch

git checkout -b feature/auth-login



\### 3. Work on the feature



Make the required code or documentation changes.



\### 4. Commit changes

git add .

git commit -m "Add auth login feature"



\### 5. Push feature branch

git push -u origin feature/auth-login



\### 6. Create Pull Request



Create a Pull Request from:



feature/auth-login → develop

\### 7. Merge after review



Once reviewed and tested, merge into develop.



Naming Convention



Examples:



feature/auth-login

feature/create-reminder

feature/document-upload

feature/checklist-engine

feature/notification-design

Rule



No direct commits to main once development starts.



All work must go through develop and feature branches.







