---
title: Production Pipeline Management System
subtitle: Workflow management system for animation production
start_date: 2013-06-01
end_date: 2015-12-31
role: Full-stack Developer
technologies:
  - CentOS Linux
  - Nginx
  - PHP 5.6
  - CodeIgniter 3
  - MySQL 5.4
  - jQuery 2.2.2
  - Bootstrap 3
---

## Project Overview

Developed a **Production Pipeline Management System** to comprehensively manage animation production workflows.
The system was designed to systematically manage various workflows in TV animation production, **significantly improving production efficiency**.

Throughout the project period, I handled all development processes from planning to database design, frontend and backend development.

## Core Features

- Project management (Series/Season/Episode)
- Asset management (characters, backgrounds, props, etc.)
- Shot management (tracking cut status and work progress)
- Task lists and artist workload tracking
- Confirmation list and approval process management
- Notification system
- Overall production workflow monitoring

## Technical Implementation

### System Architecture & Backend
- Built server environment on CentOS
- Configured lightweight operations using Nginx + PHP 5.6
- Ensured maintainability with CodeIgniter 3-based MVC architecture
- Designed database with MySQL 5.4 for projects, assets, shots, users, and work history
- Implemented RESTful data processing logic

### Frontend
- Implemented interactions based on jQuery 2.2.2
- Built responsive UI using Bootstrap 3
- Designed data visualization and status display UI for each production stage

### Operations & Workflow Management
- Saved status changes, artist assignments, and confirmation records for each production stage
- Optimized data structure to quickly identify bottlenecks in each workflow
- Managed workflows for all teams (original art, background, modeling, animation teams, etc.) in a single system

## Achievements

- Systemized manually-managed and Excel-based workflows, **significantly improving production efficiency**
- Real-time access to shot/asset/work status increased inter-team communication speed
- Systematic approval (confirmation) process **reduced work delays and omissions**
- At-a-glance workflow status reduced PM's project management burden

## Technical Challenges & Solutions

Due to the complex relationships between shots/assets/artists in animation production,
data model design was the biggest challenge.

To solve this:

- Systematically redesigned the relationships between **Shot, Asset, and Task** entities through normalization
- Managed state values and history in separate tables to enable workflow change tracking
- Recorded all changes in assignments, confirmations, and work status to enable root cause analysis when issues occur

Thanks to this structure, I completed a system that could be continuously and stably utilized even in large-scale animation projects.
