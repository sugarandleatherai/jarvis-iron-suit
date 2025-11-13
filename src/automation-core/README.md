# Automation Core

This directory contains the core automation engine and workflow orchestration system for the Jarvis Iron Suit project.

## Overview

The automation core is responsible for:
- Workflow orchestration and execution
- Event processing and routing
- State management and persistence
- Integration with external systems

## Structure

```
automation-core/
├── workflow-engine/       # Core workflow execution engine
├── event-processor/       # Event handling and routing
├── state-manager/         # State persistence and management
├── integration-adapter/   # External API integrations
└── utils/                 # Shared utilities
```

## Getting Started

### Installation
```bash
npm install
```

### Configuration
Copy `.env.example` to `.env` and configure:
```bash
cp .env.example .env
```

### Running Tests
```bash
npm test
```

### Development
```bash
npm run dev
```

## Key Components

### Workflow Engine
Orchestrates the execution of automated workflows with support for:
- Sequential and parallel execution
- Conditional branching
- Error handling and retries
- Workflow state management

### Event Processor
Handles incoming events and routes them to appropriate handlers:
- Event validation and parsing
- Priority-based processing
- Dead letter queue for failed events
- Event logging and monitoring

### State Manager
Manages workflow and system state:
- Persistent state storage
- State transitions and history
- Rollback capabilities
- State recovery mechanisms

## API Documentation

See [API.md](./docs/API.md) for detailed API documentation.

## Contributing

Please read [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines.

## License

See [LICENSE](../../LICENSE) file.
