# CallLock Core Development Guidelines

## Project Mission
Build a Done-For-You automation platform that captures missed calls for trades/service businesses and converts them into booked appointments using AI-powered SMS conversations.

## Development Standards

### Code Quality
- All n8n workflows must include error handling nodes
- Use descriptive node names (e.g., "Extract Phone Number" not "Extract")
- Include comments for complex logic
- Test all webhook endpoints with real data

### Performance Requirements
- SMS response time: < 5 seconds
- AI response time: < 10 seconds
- System uptime: 99.9% during business hours
- Handle 100 concurrent conversations

### Security Standards
- Encrypt all sensitive data at rest
- Use environment variables for API keys
- Implement TCPA compliance for SMS
- Validate all webhook inputs

### Documentation Requirements
- Document all workflow changes
- Update feature registry for each completed feature
- Include troubleshooting steps for common issues
- Maintain API credential setup guides

## Workflow Naming Convention
- WF-01: Missed Call Intake
- WF-02: SMS Conversation Handler
- WF-03: Status Handler
- WF-04: Abandonment Recovery
- WF-05: Second Follow-up

## Error Handling Standards
- Retry failed API calls 3x with exponential backoff
- Log all errors to monitoring system
- Create CRM tasks for manual intervention
- Send Slack alerts for critical failures

## Testing Requirements
- Test with real phone numbers before production
- Validate all state machine transitions
- Test error scenarios (API failures, invalid inputs)
- Load test with 100+ concurrent users

## Deployment Checklist
- [ ] All workflows tested in staging
- [ ] Error handling verified
- [ ] Monitoring alerts configured
- [ ] Documentation updated
- [ ] Client onboarding guide ready
