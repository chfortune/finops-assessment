# FinOps Assessment Tool

## Overview

This project provides a comprehensive FinOps maturity assessment tool based on the official FinOps Foundation framework. The tool enables organizations to evaluate their cloud financial operations maturity across the four official domains and their associated capabilities.

## Structure

### Data Files

- **`finops_capabilities.json`** - Main data file containing:
  - Official FinOps domains (4 domains)
  - Capabilities organized by domains
  - Assessment criteria for each maturity level (Crawl, Walk, Run, Fly)
  - Indicators, gaps, next steps, and KPIs for each capability

### Generated Files

- **`finops_scoring.html`** - Interactive web-based assessment interface

## Features

### Assessment Interface

- **Domain-based organization**: Questions organized by the 4 official FinOps domains
  - Understand Usage & Cost
  - Quantify Business Value  
  - Optimize Usage & Cost
  - Manage the FinOps Practice

- **Maturity levels**: Each capability assessed across 4 levels:
  - Level 1: Crawl (0-25 points)
  - Level 2: Walk (26-50 points)
  - Level 3: Run (51-75 points)
  - Level 4: Fly (76-100 points)

- **Interactive scoring**: 
  - Yes/No questions for each indicator
  - Real-time score calculation
  - Visual progress indicators

### Data Management

- **Local storage**: Assessment responses automatically saved to browser local storage
- **Export/Import**: Save and load assessment results as JSON files
- **Clear storage**: Reset all assessment data

### Visualization

- **Dashboard views**: Overall scores and maturity levels
- **Domain breakdown**: Scores by domain with color-coded indicators
- **Capability details**: Detailed assessment results for each capability

## Usage

1. **Open the assessment**: Load `finops_scoring.html` in a web browser
2. **Set assessment date**: Enter the date of the assessment
3. **Complete questions**: Go through each domain and capability, answering Yes/No questions
4. **Review results**: View calculated scores and maturity levels
5. **Export results**: Save assessment data for future reference

## Technical Implementation

### JSON Structure

The assessment data follows this hierarchy:
```
finops_capabilities/
├── domains/
│   ├── understand_usage_cost/
│   │   └── domains_capabilities/
│   │       ├── capability_name/
│   │       │   └── capabilities/
│   │       │       ├── level_1_crawl/
│   │       │       ├── level_2_walk/
│   │       │       ├── level_3_run/
│   │       │       └── level_4_fly/
```

### Key Components

- **Indicators**: Specific observable behaviors or practices
- **Gaps**: Description of what's missing at each maturity level
- **Next steps**: Recommended actions for improvement
- **KPIs**: Key performance indicators for measurement

## Recent Updates

- Updated JSON structure to use official FinOps domains
- Renamed keys for clarity: "assessments" → "capabilities", "capabilities" → "domains_capabilities"
- Simplified interface by removing evaluator, organization, and overview fields
- Enhanced local storage functionality for data persistence
- Improved error handling and user feedback

