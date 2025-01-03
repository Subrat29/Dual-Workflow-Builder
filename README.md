# Dual Workflow Builder Documentation

## Overview
A Next.js application that combines a visual workflow builder with report generation capabilities. The application allows users to create, edit, and manage workflows through both a visual interface and natural language queries.

## Project Structure
```
src/
├── components/
│   ├── ReportGenerator/
│   │   ├── chart-component.jsx     # Chart visualization components
│   │   ├── draggable-element.jsx   # Draggable elements for report builder
│   │   └── Sidebar.jsx            # Sidebar component for report builder
│   ├── ui/                        # Reusable UI components
│   └── WorkflowBuilder/           # Workflow builder components
│       ├── draggable-node.tsx     # Draggable nodes for workflow
│       ├── natural-language-query.tsx # NLP input component
│       ├── node-category.tsx      # Node categorization component
│       ├── pipeline-ui.tsx        # Pipeline visualization
│       ├── workflow-layout.tsx    # Main layout for workflow builder
│       └── nodes/                 # Node type implementations
├── config/
│   ├── default-report.ts         # Default report configuration
│   └── default-workflow.ts       # Default workflow configuration
├── hooks/                        # Custom React hooks
├── lib/                         # Utility functions
├── nlp/                         # Natural Language Processing logic
└── redux/                       # State management
```

## Features

### 1. Workflow Builder
- Visual workflow creation interface
- Natural language query support to generate workflows
- Node types:
  - Input nodes
  - Output nodes
  - Typeform integration
  - AI processing
  - List operations
  - File generation
  - Analysis nodes

### 2. Report Generator
- Drag-and-drop report building
- Chart component integration
- Support for multiple visualization types
- Preview capabilities

### 3. User Interface
- Responsive design (mobile/desktop layouts)
- Customizable sidebar
- Tooltips for better UX
- Tab-based navigation
- Resizable panels

## Key Components

### WorkflowLayout
- Main layout component for the workflow builder
- Features:
  - Workflow management
  - Node library
  - Save/Share capabilities 
  - Settings management
  - Report preview

### Node System
Built-in node types:
- Input/Output nodes
- Typeform submission reader
- AI processing nodes
- List manipulation nodes
- File generation nodes
- Analysis nodes

### State Management
Uses Redux for state management:
- Workflow state
- Node configurations
- UI state

## Default Configurations

### Default Workflow
Example implementation: Employee Satisfaction Survey Analysis
```javascript
{
  name: "Employee Satisfaction Survey Analysis",
  nodes: [
    {
      id: "typeform-1",
      type: "typeform",
      // Configuration for survey data collection
    },
    {
      id: "ai-1",
      type: "askAI",
      // AI analysis configuration
    },
    {
      id: "file-1",
      type: "generateFile",
      // Report generation settings
    }
  ]
}
```

## Usage

### Creating a Workflow
1. Access the workflow builder
2. Choose between:
   - Visual node-based creation
   - Natural language query input
3. Configure nodes and connections
4. Save and test the workflow

### Generating Reports
1. Navigate to report generator
2. Add desired components
3. Configure visualizations
4. Preview and export the report

## Technical Implementation
- Built with React + Next.js framework
- Uses Shadcn for UI components
- Redux for state management
- Natural language processing for workflow generation
- Responsive design with mobile-first approach

This documentation provides an overview of the project's structure and main features. For specific implementation details, refer to the individual component files in the source code.