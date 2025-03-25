# Analytics Team Repository

## Overview
This is a suggested analytics ways of working for Cash Rewards. It follows structured organization principles to promote code reuse, collaboration, and maintainability across SQL development, Airflow orchestration, and Power BI dashboard creation and maintenance.

## Repository Structure
```
cash-rewards-analytics/
├─Epic/
├── projects/
│ ├── JIRATICKET-proj-/
│ | ├── Redshift/
│ | | ├───  Inputs/
│ | | ├───  Outputs/
│ | | ├───  Reports/
│ | | | ├───  Deployment/
│ | | | ├───  DEV/
│ | | | ├───  PROD/
│ | | ├───  Scripts/
│ | | | ├───  Deployment/
│ | | | ├───  DEV/
│ | | | ├───  PROD/
│ | ├── SQL/
│ | | ├───  Input/
│ | | ├───  Output/
│ | | ├───  Report/
│ | | ├───  Scripts/
│ | | | ├───  Deployment/
│ | | | ├───  DEV/
│ | | | ├───  PROD/
│ │ ├── documentation/ # Confluence Integration?
│ │ └── airflow/ # Procedure Orchestration
│ │ ├── ...
│ └── ...
├── shared/
| ├── Theme_templates
| ├── helper_Scripts
| ├── past_analysis
| ├── Project_template
└── docs/
```

# Starting a New Project
1. **Create your project folder**:
   - Clone repo locally
   - In jira make sure to create a parent ticket that will house all tasks of the project, this ticket number will be what is referenced on the GIT parent folder
   - navigate to the appropriate epic folder 
   - Create a new project folder
   - Name it `JIRATICKET-proj` (replace with ticket number of parent ticket created)
   - for any sub tasks under the parent use this ticket number when entering in new files to the project. IE if project number is DA-1111 then you create a subtask (DA-1112) to add some new scripts the scripts will be DA-1112-STORED_PROCEDURE_testscript stored under the DA-1111 project folder 
   - commit the change

2. **Copy the template structure**:
   - Go to `shared/Project_template/`
   - Copy the folders into your project folder 
   

# Why We Want to Use Airflow

* **Breaking Down Complexity**: Airflow transforms monolithic SQL scripts into manageable, modular tasks that are easier to maintain, debug, and collaborate on - allowing team members to work on different components simultaneously.

* **Improved Reliability and Performance**: Tasks can be scheduled intelligently, run in parallel when possible, and automatically retry when failures occur - reducing overall processing time and eliminating the need to restart entire workflows when errors happen.

* **Better Visibility and Control**: The Airflow UI provides clear visualization of workflow progress, execution history, and performance metrics - creating natural documentation and making it easier to identify and resolve bottlenecks in complex data pipelines.

