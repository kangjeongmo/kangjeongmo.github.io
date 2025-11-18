---
title: Asset Search Program
subtitle: Asset search and management system for animation production
start_date: 2016-01-01
end_date: 2016-04-30
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

I independently developed an **Asset Search System**
that can quickly search and manage numerous assets (characters, backgrounds, props, etc.)
needed in the animation production process.

I built an efficient search environment by integrating data utilized in the production management system and asset version control tool,
enabling animation artists and PMs to instantly find the information they need.

## Key Features

- Automatic asset file collection and DB update from server (crontab, daily at 6 AM)
- Asset search (filename, tag, process-based filter support)
- File server path display
- File download feature
- Image preview / detail view
- Tag feature (add, delete, search)
- Maya / 3ds Max file type distinction display
- Animation process status display (design, modeling, rigging, etc.)

## Technical Implementation

### Data Collection Automation

- Periodically scanned server asset files
  to daily reflect folder structure and metadata in DB in latest state
- Performed **automatic synchronization work daily at 6 AM** using Linux `crontab`
- Normalized and stored file extensions, paths, modification dates, process information, etc.

### Backend

- Nginx + PHP 5.6 environment configuration
- Development with CodeIgniter 3-based MVC structure
- Fast inquiry of even large-scale data through asset search query optimization
- MySQL-based table design and search index application

### Frontend

- jQuery-based interaction implementation
- Bootstrap 3-based responsive UI construction
- Asset preview in image list/grid format
- UI composition for process-based tags and filters

## Achievements

- Systematized work of manually finding asset locations,
  **significantly improving work inquiry speed**
- Increased artist work efficiency with tag-based search and process-based filters
- Reduced file management confusion, and **significantly improved asset accessibility**
  across entire animation pipeline
- Smooth work sharing among multiple teams including modelers, riggers, and animators

## Technical Challenges and Solutions

Since asset file types varied (2D/3D/images/project files)
and folder structures operated differently by project,
creating a consistent DB structure was a major challenge.

To solve this, I:

- Created category rules based on file extensions
- Separated processing logic by DCC tool (Maya / 3ds Max, etc.)
- Improved search accuracy by introducing tag system
- Optimized data synchronization logic
  to enable fast scanning and storage of even large-scale file structures

Through this, I **dramatically reduced asset search and inquiry time
across the entire animation production pipeline**.
