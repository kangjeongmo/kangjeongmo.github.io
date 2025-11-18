---
title: Traffic Checker
subtitle: Electron-based mod_cband traffic monitoring Windows application
start_date: 2022-08-01
end_date: 2022-08-31
role: Developer
technologies:
  - Electron
  - Node.js
  - Axios
  - Cheerio
  - TailwindCSS
---

## Project Overview

Independently developed a **Traffic Monitoring Program (Traffic Checker)** that automatically crawls traffic usage information from the server's **mod_cband status page** and visualizes it in an easy-to-read format in a Windows desktop environment.

Delivered as a Windows app using Electron,
parsing the mod_cband status page using Axios and Cheerio in a Node.js environment.
Used TailwindCSS to build an intuitive and fast UI.

## Core Features

- Automatic crawling of mod_cband status pages
- Parsing traffic usage (upload/download/current usage)
- Electron-based Windows application
- Clean UI based on TailwindCSS
- Real-time query/refresh functionality
- Scalable structure to register and monitor multiple servers

## Technical Implementation

### Data Collection / Crawling

- **Axios** to request mod_cband status page
- **Cheerio** to parse HTML structure and extract traffic usage
- Considering the unstructured nature of HTML, combined string-based parsing with exception handling logic

### Electron-based Windows App

- Executed Node.js crawler in Electron main process
- Displayed UI and data in renderer process
- Delivered crawling results to UI via IPC communication
- Packaged as easy-to-run Windows executable (.exe) for users

### UI / Design

- Quickly and lightly styled UI with TailwindCSS
- Applied color-based highlights for at-a-glance traffic status (e.g., warning colors for high usage)
- Configured list to register and monitor multiple servers

## Achievements

- **Real-time traffic status monitoring from Windows app** without needing to open web browser each time
- Provided Electron-based format that anyone can install and run
- Increased server administrators' work efficiency
- Transformed inconvenient text-format data from mod_cband status page into user-friendly UI

## Technical Challenges & Solutions

The mod_cband page has unstandardized HTML text structure,
making accurate traffic number extraction most challenging.

To solve this:

- Parsed HTML like DOM with Cheerio, then stably extracted only needed numbers through pattern analysis
- Added exception handling and retry logic for Axios request failures
- Used Electron's main process and renderer IPC structure to clearly separate data flow and ensure maintainability

As a result, built a lightweight traffic checking program that cleanly extracts needed data from complex HTML and stably delivers it to Windows UI.
