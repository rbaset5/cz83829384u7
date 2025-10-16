# MCP Commands Reference

## Overview
Model Context Protocol (MCP) commands for CallLock n8n automation workflows.

## Available Commands

### Workflow Management
- `mcp_n8n_get_workflow` - Retrieve workflow configuration
- `mcp_n8n_create_workflow` - Create new workflow
- `mcp_n8n_update_workflow` - Update existing workflow
- `mcp_n8n_delete_workflow` - Delete workflow
- `mcp_n8n_execute_workflow` - Execute workflow manually

### Data Management
- `mcp_google_sheets_append_row` - Add lead data to sheets
- `mcp_google_sheets_update_row` - Update lead status
- `mcp_google_sheets_get_data` - Retrieve lead information
- `mcp_close_crm_create_task` - Create CRM task
- `mcp_close_crm_update_contact` - Update contact information

### Communication
- `mcp_twilio_send_sms` - Send SMS message
- `mcp_twilio_get_message_status` - Check delivery status
- `mcp_slack_send_message` - Send alert to Slack

### AI Integration
- `mcp_openai_chat_completion` - GPT-4 conversation handling
- `mcp_openai_moderation` - Content moderation

### Calendar Integration
- `mcp_google_calendar_check_availability` - Check time slots
- `mcp_cal_com_create_booking` - Create appointment booking

## Usage Examples

### Send SMS Response
```javascript
await mcp_twilio_send_sms({
  to: "+1234567890",
  from: "+1987654321",
  body: "Thanks for calling! What service do you need?"
});
```

### Create Lead Record
```javascript
await mcp_google_sheets_append_row({
  spreadsheetId: "leads_sheet_id",
  range: "Sheet1!A:Z",
  values: [
    ["LEAD_1234567890", "+1234567890", "AWAITING_SERVICE_TYPE", 1, "", "", "", new Date().toISOString(), false, false, false, false, new Date().toISOString(), "", ""]
  ]
});
```

### Check Calendar Availability
```javascript
const availability = await mcp_google_calendar_check_availability({
  calendarId: "primary",
  timeMin: "2024-01-20T09:00:00Z",
  timeMax: "2024-01-20T17:00:00Z"
});
```

## Error Handling
All MCP commands should be wrapped in try-catch blocks with appropriate error handling:

```javascript
try {
  const result = await mcp_command_name(params);
  // Process successful result
} catch (error) {
  console.error(`MCP command failed: ${error.message}`);
  // Create fallback task or alert
}
```

## Rate Limits
- Twilio SMS: 1 message per second per number
- OpenAI API: 3 requests per minute
- Google Sheets: 100 requests per 100 seconds
- Google Calendar: 1000 requests per 100 seconds

## Authentication
All MCP commands require proper authentication tokens:
- Twilio: Account SID and Auth Token
- OpenAI: API Key
- Google: OAuth2 credentials
- Close CRM: API Key
