---
title: Daily Worklog Program
subtitle: Studio's departmental work and schedule management system
start_date: 2016-04-01
end_date: 2016-08-31
role: Full-stack Developer
technologies:
  - CentOS Linux
  - Nginx
  - PHP 5.6
  - CodeIgniter 3
  - MySQL 5.4
  - jQuery 2.2.2
  - AngularJS 1.4.9
  - Bootstrap 3
---

## Project Overview

I independently developed a Daily Worklog System
to **systematize daily work management and leave management**
for the company's production teams (design, modeling, rigging, animation, etc.).

I improved the system so that daily work records, workload aggregation, and leave application details,
previously shared via files or verbally,
could all be managed in a web-based system.

I performed the entire development process as a solo developer,
from planning to DB design, frontend and backend development.

## Key Features

- Daily worklog creation by department
  - Production management / Design / Modeling / Rigging / Animation / Lighting
- Individual workload management
- Leave management feature (annual leave, half-day leave registration and recording)
- Administrator statistics dashboard
  - Workload by department
  - Workload by individual
  - Period-based inquiry
- Excel Export feature
- Search/filter-based work inquiry

## Technical Implementation

### Backend

- CentOS + Nginx-based server environment construction
- Functional unit module design with CodeIgniter 3-based MVC architecture
- MySQL 5.4 table structure design for department/individual/workload/leave
- Data communication with AngularJS frontend through REST-style API construction

### Frontend

- UI implementation in SPA format based on AngularJS 1.4.9
- Auxiliary interaction composition with jQuery 2.2.2
- Responsive UI composition with Bootstrap 3
- Data-based screen implementation including real-time filtering and period search
- Excel Export UI and download feature provision

### Operation and Management Features

- Work status visualization with dashboard by department/individual
- Leave application history management and administrator approval feature
- Statistics inquiry by period/user
- Utilization for billing work and project schedule management

## Achievements

- Systematized daily work reporting and leave management,
  **increasing communication efficiency across all departments**
- Easy PM schedule management and resource allocation
  with visual workload confirmation
- Reduced report creation time
  through Excel Export feature
- Enabled long-term production efficiency analysis
  with database-recorded work records
- Significantly reduced issues like work omissions and leave record errors

## Technical Challenges and Solutions

Since each department has different work types,
it was not easy to handle worklogs with a single structure.

To solve this, I:

- Designed DB with common fields + department-specific extension field structure
- Dynamically changed input UI based on AngularJS
- Strengthened reusability and maintainability
  by modularizing features like data filtering and period search

This enabled consistent management of various types of departmental work
within one integrated system.
