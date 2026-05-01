# FinOps Assessment Tool

## Overview

This project provides a comprehensive FinOps maturity assessment tool based on the official FinOps Foundation Framework. The tool enables organizations to evaluate their cloud financial operations maturity across the four official domains and their associated capabilities with detailed assessments and deliverables.

## Structure

### Data Files

- **[`finops_capabilities_extended.json`](./finops_capabilities_extended.json)** - Main data file containing:
  - Official FinOps domains (4 domains)
  - 21 capabilities organized by domains
  - Assessment criteria for each maturity level (Crawl, Walk, Run)
  - 184 assessments with evidence examples
  - 189 deliverables with formats and descriptions
  - KPI targets for each maturity level
  - Detailed descriptions and use cases

### Generated Files

- **[`finops-scoring-model.html`](./finops-scoring-model.html)** - Interactive web-based assessment interface

## Features

### Assessment Interface

- **Domain-based organization**: Questions organized by 4 official FinOps domains
  - Understand Usage & Cost (4 capabilities)
  - Quantify Business Value (5 capabilities)
  - Optimize Usage & Cost (5 capabilities)
  - Manage the FinOps Practice (7 capabilities)

- **Maturity levels**: Each capability assessed across 3 levels:
  - Level 1: Crawl (0-1 point)
  - Level 2: Walk (2 points)
  - Level 3: Run (3 points)
  - Overall scoring: 0-3 points per capability

- **Interactive scoring**: 
  - Yes/Partial/No/N/A questions for each assessment
  - Real-time score calculation
  - Visual progress indicators
  - Evidence examples for each assessment
  - Deliverables tracking by maturity level

### Data Management

- **Local storage**: Assessment responses automatically saved to browser local storage
- **Export/Import**: Save and load assessment results as JSON files
- **Clear storage**: Reset all assessment data
- **Auto-save**: Automatic saving after each response

### Visualization

- **Dashboard views**: Overall scores and maturity levels with color-coded rings
- **Domain mini-cards**: Real-time domain scores with progress bars
- **Radar chart**: Four-domain visual representation of maturity
- **Capability details**: Detailed assessment results with deliverables and KPIs
- **Progress tracking**: Completion percentage and counters

## Usage

### For End Users

1. **Open assessment**: Load [`finops-scoring-model.html`](./finops-scoring-model.html) in a web browser
2. **Set assessment date**: Enter date of assessment
3. **Complete questions**: Go through each domain and capability, answering Yes/Partial/No/N/A questions
4. **Review deliverables**: Check required deliverables for each maturity level
5. **Monitor KPIs**: Track progress against target KPIs
6. **View results**: Analyze radar chart and domain breakdowns
7. **Export results**: Save assessment data for future reference

## Technical Implementation

### JSON Structure

The assessment data follows this hierarchy:
```
finops_capabilities_extended.json
├── framework/
│   ├── version
│   ├── description
│   └── domains
│       ├── understand/ (4 capabilities)
│       ├── quantify/ (5 capabilities) 
│       ├── optimize/ (5 capabilities)
│       └── manage/ (7 capabilities)
│           └── capabilities/
│               ├── id, abbr, name, description
│               └── maturity/
│                   ├── crawl/
│                   │   ├── description
│                   │   ├── deliverables[]
│                   │   ├── assessments[]
│                   │   └── kpi_targets
│                   ├── walk/
│                   └── run/
└── usage/
    ├── description
    ├── scoring_model
    ├── recommended_cadence
    └── totals (capabilities, assessments, deliverables)
```

## Recent Updates

### Major Enhancements (2024)

- **Extended Framework**: Expanded from 10 to 21 capabilities across 4 domains
- **New Domain**: Added "Manage the FinOps Practice" with 7 capabilities
- **Enhanced Assessments**: 184 assessments with evidence examples and partial scoring
- **Deliverables Tracking**: 189 deliverables with specific formats and descriptions
- **KPI Integration**: Target metrics for each maturity level
- **Improved UI**: Modern design with radar chart, progress indicators, and responsive layout
- **Better Data Model**: Structured JSON with clear hierarchy and validation rules

### Technical Improvements

- **Fixed JavaScript errors**: Resolved `updateLevel` function name and JSON parsing issues
- **Enhanced styling**: Improved badges, colors, and visual hierarchy
- **Better UX**: Auto-save, expandable sections, and intuitive navigation
- **Comprehensive scoring**: Weighted calculations with 80% thresholds
- **Export capabilities**: JSON export with complete assessment data

### Current Statistics

- **4 domains**: Understand, Quantify, Optimize, Manage
- **21 capabilities**: Comprehensive coverage of FinOps practices
- **184 assessments**: Detailed evaluation criteria
- **189 deliverables**: Concrete outputs and artifacts
- **3 maturity levels**: Crawl, Walk, Run with clear progression

