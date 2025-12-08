# Slack Integrations

This directory contains all Slack-related integrations for the Jarvis Iron Suit project.

## Overview

The Slack integrations provide:
- Slash commands for task automation
- Interactive message components
- Event subscriptions and webhooks
- Bot user functionality
- OAuth and authentication

## Structure

```
slack-integrations/
├── commands/          # Slash command handlers
├── events/           # Event subscription handlers
├── actions/          # Interactive component handlers
├── middleware/       # Authentication and validation
├── utils/            # Slack-specific utilities
└── templates/        # Message templates
```

## Getting Started

### Prerequisites
- Slack workspace with admin access
- Slack App created and configured
- Bot token and signing secret

### Installation
```bash
npm install
```

### Configuration
Configure your Slack app credentials:
```bash
cp .env.example .env
# Edit .env with your Slack credentials
```

Required environment variables:
- `SLACK_BOT_TOKEN`: Bot User OAuth Token
- `SLACK_SIGNING_SECRET`: Signing secret for request verification
- `SLACK_APP_TOKEN`: App-level token (for Socket Mode)

### Running Locally
```bash
npm run dev
```

### Running Tests
```bash
npm test
```

## Available Commands

### Slash Commands
- `/jarvis help` - Show available commands
- `/jarvis status` - Check system status
- `/jarvis task create <description>` - Create a new task
- `/jarvis task list` - List all tasks
- `/jarvis workflow start <name>` - Start a workflow

## Webhook Configuration

### Request URL
Configure in Slack App settings:
- **Development**: `https://your-dev-url/slack/events`
- **Production**: `https://your-prod-url/slack/events`

### Event Subscriptions
Subscribe to the following events:
- `message.channels` - Messages in public channels
- `app_mention` - Direct mentions of the bot
- `reaction_added` - Reactions to messages

### Interactive Components
Configure request URL for interactive components:
- `https://your-url/slack/actions`

## Message Templates

### Block Kit
We use Slack's Block Kit for rich message formatting. Templates are in `templates/`:
- `notification.js` - Standard notification format
- `task-card.js` - Task card with actions
- `status-report.js` - Status report format

Example:
```javascript
const { taskCard } = require('./templates/task-card');
const message = taskCard({
  title: 'New Task',
  description: 'Task description',
  assignee: '@user'
});
```

## Authentication & Security

### Request Verification
All incoming requests are verified using Slack's signing secret:
```javascript
const { verifySlackRequest } = require('./middleware/auth');
app.use('/slack/*', verifySlackRequest);
```

### OAuth Flow
For multi-workspace installation:
1. User initiates OAuth
2. Redirect to Slack authorization
3. Handle callback and store tokens
4. Bot is ready to use

## Error Handling

### Common Issues
1. **Invalid signing secret**: Check environment variables
2. **Token expired**: Refresh OAuth token
3. **Rate limiting**: Implement exponential backoff
4. **Network errors**: Retry with timeout

### Error Responses
All errors are logged and reported to monitoring:
```javascript
try {
  await sendMessage(channel, message);
} catch (error) {
  logger.error('Failed to send message', error);
  await sendErrorNotification(error);
}
```

## Testing

### Unit Tests
```bash
npm test
```

### Integration Tests
```bash
npm run test:integration
```

### Manual Testing
Use the `#jarvis-testing` channel for manual testing.

## Deployment

### Staging
```bash
npm run deploy:staging
```

### Production
```bash
npm run deploy:production
```

## Monitoring

### Metrics
- Command usage counts
- Response times
- Error rates
- Active users

### Alerts
Configure alerts for:
- High error rates
- Slow response times
- Failed webhooks
- Authentication failures

## Resources

- [Slack API Documentation](https://api.slack.com/)
- [Block Kit Builder](https://api.slack.com/block-kit)
- [Bolt Framework](https://slack.dev/bolt-js/)

## Contributing

Please read [CONTRIBUTING.md](../../CONTRIBUTING.md) for guidelines.

## License

See [LICENSE](../../LICENSE) file.
