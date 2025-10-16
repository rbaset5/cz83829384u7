# PRD Validation Checklist

## Before Each Commit
Ask yourself:
- Does this align with PRD MVP scope?
- Does this complete a user story?
- Does this meet acceptance criteria?
- Is this measuring a KPI?

## Before Marking Feature DONE
Verify against PRD:
- [ ] Functional requirement met
- [ ] Performance SLA achieved
- [ ] Error handling implemented
- [ ] Monitoring in place
- [ ] Documentation updated

## Quick PRD Lookups
- Scope: `docs/PRD_MVP_V1.md#out-of-scope-for-mvp`
- KPIs: `docs/PRD_MVP_V1.md#success-metrics`
- Timeline: `docs/PRD_MVP_V1.md#implementation-timeline`
- Acceptance: `docs/PRD_MVP_V1.md#mvp-acceptance-criteria`

## Feature Completion Checklist

### For Each User Story
- [ ] Acceptance criteria met
- [ ] Performance requirements satisfied
- [ ] Error scenarios handled
- [ ] Integration tested
- [ ] Documentation updated

### For Each Workflow
- [ ] Webhook validation implemented
- [ ] Error handling nodes added
- [ ] Retry logic configured
- [ ] Logging implemented
- [ ] Real data testing completed

### For Each Integration
- [ ] API credentials secured
- [ ] Rate limits respected
- [ ] Error responses handled
- [ ] Fallback mechanisms in place
- [ ] Monitoring alerts configured

## PRD Compliance Check

### MVP Scope Validation
- [ ] Feature is in MVP scope (not in out-of-scope list)
- [ ] Supports single location only
- [ ] Uses SMS communication only
- [ ] English language only
- [ ] No voice AI involved

### Performance Validation
- [ ] SMS response < 5 seconds
- [ ] AI response < 10 seconds
- [ ] System uptime 99.9%
- [ ] Handles 100 concurrent users
- [ ] Error rate < 1%

### Security Validation
- [ ] Data encrypted at rest
- [ ] API keys in environment variables
- [ ] TCPA compliance for SMS
- [ ] Input validation implemented
- [ ] No sensitive data in logs

## Weekly Review Questions
1. Are we on track for this week's goals?
2. Which user stories are blocked?
3. What acceptance criteria need attention?
4. Are we measuring the right KPIs?
5. What risks need mitigation?
