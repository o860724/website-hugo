---
title: "BPM system"
date: 2023-01-06T01:00:37+08:00
draft: false
---

Our BPM system is based on the e-form requirements of the HRM system. We aim to expand more comprehensive functions to help organizations establish, execute, monitor, and optimize their business processes.<!--more-->
We virtualize physical business processes by using forms and flows, which we call "tasks." The task manager can establish a new task on the backstage. Then, collecting essential information via form, assigning responsible owners through flow setting, and controlling users' roles for each task, such as task applicant, viewer, manager, or monitor. Users can then easily start or execute an approval process on the forestage (supporting mobile and web).

User accounts are linked to our HRM system. Furthermore, we support to set a specific ‘virtual organization’ for the collaborative task which helps cross-functional teamwork become much easier.

# **Main Feature**
Forestage: Execute the business processes(task)
- Apply new task
- My task list
- My application
- My approval
- Info. center

Backstage: Establish the business process(task), organization and administration
- Business Process (Task) Design: form, flow engine, task access control
- Organization: virtual organization, account management
- Administration: access level setting, change log

# **My Role**
- Product Manager(Focus on Task Execution/Flow Engine)

# **My Tool**
- Trello
- Figma
- Notion

# **Function Map**
![User Flow](https://drive.google.com/uc?export=view&id=1DLXD_RQCRtQ958kquhnsRsov4Hcv6rzq)

# **Task Execution/Flow Engine**
## 3 critical elements for Flow Process:
- Owner
- Operation
- Node Status
![Flow Engine](https://drive.google.com/uc?export=view&id=1_QSWdw8UnDRFhGuPNAFdNrQpOGY_EXp7)

## User Operation & Flow Process List
|Operation|Flow direction|Operation node|Operation node status|Next node status|Pass by node status|
| --- | --- | --- | --- | --- | --- |
| Submit/ Approve | Downstream flow to next node | In-progress node | In progress →Completed | Unprocessed →in progress | N/A |
| Submit/ Approve | Downstream flow to end point | In-progress node | In progress →Completed | End point(Flow completed) | N/A |
| Reject | Downstream flow to end point | In-progress node | In progress →Completed | End point(Flow completed) | In progress →unprocessed(Keep owners) |
| Return | Upstream flow to assigned node | In-progress node | In progress →Unprocessed(Free owners) | Completed→in progress(Update owners) | In progress/ completed →unprocessed(Free owners) |
| Withdraw | Upstream flow to the previous node | Previous node of  in-progress node | Completed →in progress | *Next node= operation node | *Original processing node: in progress →unprocessed(Free owners) |

## Node status Definition
| Node status | Definition |
| --- | --- |
| Unprocessed | The node is unprocessed in the flow. When the node status transfer to unprocessed, there is no owner of the node. (The owners haven’t been fetched or have been freed, except for "reject") |
|  | The task does’t exist in any user’s ‘My task list’. |
| In-progress | The node is in-progress in the flow. When the node status transfer to in-progress, the system fetch the owners of the node and send the task to the owners’ ‘My task list’ |
|  | The task exists in the owners’ ‘My task list’. |
| Completed | The node is completed in the flow. When node owners have operated  on the node, the node status transfers to completed and the node owners are fixed. |
|  | If it's a starting point, the task exists in the applicant's "My application". If it's a process node, the task must exists in at least one of the owners’ "My approval". |
