# PRD Quick Reference for AI Context

## Current Development Phase
Week 1: Foundation (Building Core Infrastructure)

## Today's Acceptance Criteria
- [ ] Twilio webhook setup complete
- [ ] WF-01 Intake workflow functional
- [ ] Google Sheets structure created
- [ ] Test with real phone numbers

## Active User Stories
- US-001: Instant SMS response (WF-01 setup)
- US-004: Landline detection (carrier lookup)
- US-005: After-hours routing (time-based logic)

## Out of Scope (Don't Build)
- Voice AI
- Email integration
- Multi-language support
- Payment processing
- Multi-location support
- Custom AI training

## Test Scenarios Required
1. Missed call → SMS sent within 5 seconds
2. Landline number → Callback task created
3. After-hours call → Appropriate messaging
4. Business hours call → Standard response
5. Invalid phone → Error handling

## Key Workflows This Week
- **WF-01: Missed Call Intake**
  - Twilio webhook trigger
  - Phone number validation
  - Carrier lookup (landline detection)
  - Business hours check
  - Initial SMS or callback task

## Success Metrics to Track
- Response Time: < 5 seconds to first SMS
- Capture Rate: 95%+ of missed calls get SMS
- Landline Detection: Accurate carrier lookup
- Business Hours: Correct time-based routing

## Common Error Scenarios
- Twilio API failure → Retry 3x with backoff
- Invalid phone number → Log and skip
- Duplicate call → Return 200 OK, no processing
- Sheets API failure → Create fallback task

## Next Week Preview
Week 2: Intelligence (GPT-4 integration, WF-02 AI Handler, state machine)
