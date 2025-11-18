---
title: Recruitment Management System
subtitle: Google OAuth-based applicant and administrator recruitment process management platform
start_date: 2019-05-01
end_date: 2019-06-30
role: Full-stack Developer
technologies:
  - HTML5
  - CSS3
  - Bootstrap 4
  - JavaScript
  - jQuery 3.4.1
  - PHP 7
  - CodeIgniter 3
  - MySQL 5.7
  - AWS EC2
---

## Project Overview

I built a **web-based Recruitment Management System**
to efficiently manage the company's recruitment process,
handling planning, development, and DB design as a solo developer.

The system was developed to handle the entire recruitment process online,
from applicant page creation to status changes, feedback recording,
Google OAuth authentication, and administrator permission separation.

## Key Features

- Google OAuth authentication-based login
- Automatic applicant page generation by job position
- Applicant information management (resume, portfolio, basic information)
- Applicant status changes (interview scheduled, on hold, pass/fail, etc.)
- Feedback recording feature (save interviewer comments)
- Result notification feature (email or status display)
- Screen and feature control based on administrator permission levels

## Technical Implementation

### Frontend

- UI construction based on HTML5 / CSS3 / Bootstrap 4
- Interaction implementation with jQuery 3.4.1
- Applicant list and status change UI by job position
- Separated pages/components displayed by permission level

### Backend

- MVC architecture based on CodeIgniter 3
- Google OAuth API integration (applicant/administrator login)
- Workflow logic construction to manage applicant status by process
- Core logic development including status changes, feedback registration, and result notification
- Secure file upload and storage structure implementation (resume/portfolio)

### Database

- MySQL 5.7-based recruitment process management structure design
- Job, Applicant, Status History, and User table composition
- Record all status change history for future analysis

### Server Environment

- PHP7 + CI3-based service deployment to AWS EC2 environment
- Basic security settings and SSH-based access permission management
- Stable operating environment configuration with Apache/Nginx

## Achievements

- Systematized previously manual recruitment procedures,
  **improving applicant management speed and accuracy**
- Increased recruitment posting management convenience with automatic applicant page generation by job position
- **Increased collaboration efficiency between interviewers and administrators**
  through status change and feedback recording features
- Simplified signup/login process with Google OAuth introduction
- Strengthened security and data access control with administrator permission separation

## Technical Challenges and Solutions

Recruitment procedures have complex characteristics with different required information by job position,
and applicant status management and feedback structures are intricately connected.

To solve this, we:

- Introduced **state and history-centered** data modeling
- Implemented template structure for automatic screen generation by job position
- Simplified authentication process and strengthened security through Google OAuth
- Recorded all status changes and feedback
  to enable immediate tracking even if disputes or errors occur later

As a result, I successfully moved the practical recruitment process online
in a short period as a single developer.
