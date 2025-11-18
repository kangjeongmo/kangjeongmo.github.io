---
title: Pension Search Platform Renewal
subtitle: Next.js-based pension search and map-based reservation platform renewal
start_date: 2023-07-01
end_date: 2023-12-31
role: Frontend Developer
technologies:
  - Adobe XD
  - Next.js 13.5.6
  - React 18.2.0
  - TypeScript 5.1.6
  - Node 20.9.0
  - Naver Maps API
---

## Project Overview

This was a complete renewal project for a domestic pension search platform,
involving comprehensive reconstruction from UI/UX redesign to frontend architecture transformation.

The project team consisted of 1 designer, 1 backend developer, and 1 frontend developer.
I was responsible for **React + Next.js-based frontend development (30% contribution)**.

We significantly improved user experience by reconstructing core features such as search performance,
map-based filtering, and time-limited deals with modern UI/UX.

## Key Features

- Pension search platform UI development
- Region-based search functionality
- Map-based search using Naver Maps API
- Pension movie clip (promotional video) playback feature
- Time-limited deals (special price time display) UI
- Full responsive frontend development

## Technical Implementation

### Frontend (My Responsibilities)

- **Next.js 13 App Router-based page composition and folder structure design**
- Developed reusable UI components with React + TypeScript
- UI/data integration for region search and map search
- Naver Maps API integration
  - Map rendering
  - Marker display
  - Search range reflection based on map movement/zoom
- Combination of Next.js Server Components + Client Components for fast page transitions
- Responsive design & mobile screen optimization

### UX / UI Implementation

- UI structure implementation based on Adobe XD design documents
- Skeleton UI applied to reduce perceived loading time
- Integrated UI composition for search results list/grid/map
- User-friendly design with filter modals, sliders, and tag-based filters

### Server Integration / State Management

- Asynchronous logic composition with fetch/Axios for API integration
- SSR data loading optimization using App Router's Server Components
- Client-side state management for search conditions (region, map range, filters, etc.)

## Achievements

- Completely replaced legacy PHP-based UI with Next.js + React,
  **significantly improving response speed, search speed, and map navigation performance**
- Greatly enhanced UX for pension search experience (list/map/search)
- Increased user search satisfaction with intuitive Naver Maps-based search flow
- Increased platform promotion utilization with time-limited deals feature
- Accurately implemented Adobe XD-based design documents,
  increasing communication efficiency between planning, design, and development teams

## Technical Challenges and Solutions

Since we had to integrate large-scale pension data with map functionality,
**search range updates and data loading optimization based on map movement** were the core challenges.

To solve this, we:

- Applied debounce to map movement events to minimize unnecessary calls
- Improved initial loading speed with Next.js Server Components-based SSR data loading
- Applied memoization at component level to minimize re-rendering
- Unified data flow management between pension list and map for UI synchronization

As a result, we successfully built a modern tourism/accommodation search platform
with fast and natural map search UX.
