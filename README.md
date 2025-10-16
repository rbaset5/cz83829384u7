# CallLock n8n Operation Workflows

## Overview
CallLock MVP v1.0 is a Done-For-You automation platform that captures missed calls for trades/service businesses and converts them into booked appointments using AI-powered SMS conversations.

## Project Structure
```
CallLock-n8n-operation-workflows/
├── docs/
│   ├── PRD_MVP_V1.md           # Product Requirements Document
│   ├── CORE_GUIDELINES.md      # Development standards
│   ├── FEATURE_REGISTRY.md     # Feature tracking
│   ├── MCP_COMMANDS.md         # MCP command reference
│   └── CHANGELOG.md            # Version history
├── .cursor/                    # Cursor AI configuration
├── workflows/production/       # n8n workflow JSON files
├── mcp/                       # MCP configuration
├── scripts/                   # Utility scripts
└── .vscode/                   # VSCode/Cursor tasks
```

## Quick Start
```bash
# Check PRD status dashboard
node scripts/prd_status.js

# Run Cursor tasks (Ctrl+Shift+P → Tasks: Run Task)
# - Check PRD Status
# - Validate Against PRD
# - Show Current Sprint
```

## Development Phase
**Current Week:** Week 1: Foundation
- Set up n8n instance
- Configure Twilio account and phone
- Create Google Sheets structure
- Build WF-01 (Intake)
- Test with real phones

## Success Metrics
- 30% missed calls → booked jobs
- < 5 second SMS response time
- 95%+ SMS delivery rate
- $5,000+ monthly revenue recovery per client

## Documentation
- [Product Requirements Document](docs/PRD_MVP_V1.md)
- [Development Guidelines](docs/CORE_GUIDELINES.md)
- [Feature Registry](docs/FEATURE_REGISTRY.md)
- [MCP Commands](docs/MCP_COMMANDS.md)