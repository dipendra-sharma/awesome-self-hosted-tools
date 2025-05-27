# OpenWA - WhatsApp Bot Automation

OpenWA is the easiest way to turn your WhatsApp into an API for bot automation.

## Features

- WhatsApp bot automation
- Message sending and receiving
- Media file handling
- Group management
- Contact synchronization
- Webhook integration
- Session management
- QR code authentication

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access OpenWA at http://localhost:8408

3. Scan the QR code with your WhatsApp mobile app

## Configuration

- Port: 8408 (maps to internal port 8080)
- Session persistence enabled
- Library version: 4.42.1

## Environment Variables

Key settings include:
- `WA_SESSION_ID`: Unique session identifier
- `WA_DISABLE_SPINS`: Disable loading animations
- `W_A_V`: Specific library version
- `WEBHOOK_URL`: URL for receiving webhooks

## Session Management

Sessions are persisted in the `/sessions` volume, allowing you to restart the container without losing your WhatsApp connection.

## API Usage

Once authenticated, you can use the API to:
- Send text messages
- Send media files
- Manage groups
- Get contact information
- Handle incoming messages via webhooks

## Important Notes

- The `--init` flag is crucial for proper zombie process cleanup
- Sessions may need re-authentication periodically
- WhatsApp may rate limit bot activities

## Volumes

- `openwa-sessions`: WhatsApp session data and configuration

## License

MIT License