# WPPConnect - WhatsApp Web API

WPPConnect is an API wrapper for WhatsApp Web that makes it easy to send and receive messages.

## Features

- Send and receive WhatsApp messages
- Media file support (images, videos, documents)
- Group management
- Contact management
- Webhook support
- Session management
- QR code generation for authentication

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access WPPConnect at http://localhost:8406

3. Scan the QR code with your WhatsApp mobile app to authenticate

## Configuration

- Port: 8406 (maps to internal port 21465)
- Session persistence via Docker volume

## Environment Variables

Key settings include:
- `SECRET_KEY`: API secret key (change for security)
- `WA_SESSION_ID`: Session identifier
- `WEBHOOK_URL`: URL for receiving webhooks
- `LOG_LEVEL`: Logging verbosity

## API Usage

Once running, you can use the REST API to:
- Send messages: POST to `/api/{session}/send-message`
- Get contacts: GET to `/api/{session}/all-contacts`
- Create groups: POST to `/api/{session}/create-group`

## Volumes

- `wppconnect-tokens`: WhatsApp session tokens
- `wppconnect-config`: Application configuration

## Security

Make sure to:
1. Change the `SECRET_KEY` to a secure value
2. Configure webhook URLs properly
3. Secure the API endpoints if exposed publicly

## License

MIT License