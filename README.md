# Automated-Task-Approval-Workflow-in-ServiceNow
This project demonstrates an automated task management and approval system built using ServiceNow. It utilizes Flow Designer, Access Controls (ACLs), and role-based user permissions to streamline the process of assigning tasks and requesting approvals.
Automated-Task-Approval-Workflow/
├── screenshots/
│   ├── flow-trigger.png
│   ├── ask-for-approval.png
│   ├── impersonate-alice.png
│   └── approval-records.png
├── update-set/
│   └── task-approval-update-set.xml
└── README.md

# ServiceNow Task Approval Workflow

This project demonstrates a custom task table with approval workflow using Flow Designer in ServiceNow.

## 🛠 Features

- Custom table `task table 2`
- ACLs controlling field-level access
- Flow triggered on creation with conditions:
  - Status = "In Progress"
  - Comments = "Feedback"
  - Assigned To = "Bob"
- Approval requested from "Alice P"
- Approval tracked via `My Approvals`


## 💾 Update Set

Includes XML export of update set: `update-set/task-approval-update-set.xml`

## 👤 Roles Used
- Admin (to configure flow, ACLs)
- Bob (task assignee)
- Alice P (approver)

---

## 📌 How to Test

1. Impersonate Bob → Create a new task
2. Status = "In Progress", Comments = "Feedback"
3. Approval goes to Alice → Impersonate her to approve
4. Status updates based on approval

