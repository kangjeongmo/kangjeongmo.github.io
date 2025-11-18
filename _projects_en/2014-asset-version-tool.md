---
title: Asset Version Control Tool
subtitle: Desktop asset management tool for Maya pipeline
start_date: 2014-09-01
end_date: 2015-07-31
role: Python Developer
technologies:
  - Python 2.7
  - Qt / PySide
  - Maya API
---

## Project Overview

Developed an **Asset Version Control Tool** for the animation production pipeline.
Provided a desktop-based tool to help Maya-based artists (modelers, riggers, animators, etc.)
manage files easily and consistently while tracking versions.

I independently led the entire process from UI/UX design to implementation and API integration,
contributing **80%** of the program structure design and core feature implementation.

## Core Features

- Asset Tree structure visualization
- Maya file server data integration
- Open / Import / Reference functionality
- Maya scene saving with automatic version management
- File preview and screenshot generation
- Version memo writing capability
- Simple automation features to improve work efficiency

## Technical Implementation

### Desktop Application
- Developed based on Python 2.7
- Built **native desktop UI** with Qt + PySide
- Directly constructed Asset Tree UI to visualize folder/file/version structure

### Maya Pipeline Integration
- Implemented Open / Import / Reference functionality using Maya API
- Automatically generated save paths according to proper Pipeline Path rules
- Seamlessly connected Maya internal commands with external server files
- Enabled artists to preview files and capture screenshots directly from Maya

### Version Control Logic
- Automatic version number increment based on file naming conventions
- Previous Version / Latest Version queries
- Version history and memo features to track workflow

## Achievements

- Significantly reduced work interruptions and file conflicts caused by file/version/path issues
- Automated manual version control, improving **work speed and accuracy**
- Standardized management of Asset, Shot, and Scene files enabled seamless work even as project scale grew
- Ultimately contributed to securing stability across the entire animation production pipeline

## Technical Challenges & Solutions

The biggest challenge was consistently connecting Maya's internal file structure
with the external server file system.

To solve this:

- Directly re-implemented Open/Import/Reference functionality using Maya commands (cmds) and API
- Unified file path rules and added validation logic to minimize file corruption/overwriting due to artist errors
- Optimized structure to quickly load even large Asset trees in Python + Qt-based desktop UI

This enabled stable and repeatable version control in Maya-based production environments.
