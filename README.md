# Analytics Team Repository

## Overview
This is a suggested analytics ways of working for Cash Rewards. It follows structured organization principles to promote code reuse, collaboration, and maintainability across SQL development, Airflow orchestration, and Power BI dashboard creation and maintenance.

## Repository Structure
```
cash-rewards-analytics/
├── projects/
│ ├── proj-JIRATICKET-lead-lag/
│ │ ├── sql/
│ │ ├── documentation/ # Confluence Integration?
│ │ ├── qa/ # Data Integrity Checks for /sql
| | ├── dashboards/ # Sharepoint Integration OR Github LFS (Large File Size)
│ │ └── airflow/ # Procedure Orchestration
| | 
│ ├── proj-JIRATICKET-cashback-rate-performance/
│ │ ├── ...
│ └── ...
├── shared/
| ├── templates
| ├── [...] # Files used by team across Projects.
└── docs/
```

# Starting a New Project
1. **Create your project folder**:
   - Go to the `projects` folder in GitHub
   - Click "Add file" → "Create new file"
   - Name it `proj_TICKET-123-project-name/README.md` (replace with actual ticket)
   - commit the change

2. **Copy the template structure**:
   - Go to `shared/templates/project_template`
   - For each folder you need:
     - Click on the folder
     - Click the "..." menu in the top-right corner
     - Select "Download" to save the folder to your computer
   - Go to your new project folder
   - Click "Add file" → "Upload files"
   - Drag and drop the downloaded folders

# Why We Want to Use Airflow

* **Breaking Down Complexity**: Airflow transforms monolithic SQL scripts into manageable, modular tasks that are easier to maintain, debug, and collaborate on - allowing team members to work on different components simultaneously.

* **Improved Reliability and Performance**: Tasks can be scheduled intelligently, run in parallel when possible, and automatically retry when failures occur - reducing overall processing time and eliminating the need to restart entire workflows when errors happen.

* **Better Visibility and Control**: The Airflow UI provides clear visualization of workflow progress, execution history, and performance metrics - creating natural documentation and making it easier to identify and resolve bottlenecks in complex data pipelines.

