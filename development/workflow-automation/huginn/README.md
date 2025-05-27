# Huginn - Workflow and Alert Automation

Huginn creates agents that monitor the web and perform actions on your behalf.

## Features

- Web scraping and monitoring
- Email notifications
- Social media automation
- Data aggregation and transformation
- Scheduled tasks
- Webhook integrations
- Custom agent creation

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Huginn at http://localhost:8403

3. Create an account and start building agents

## Configuration

- Port: 8403
- Database: MySQL 8.0
- Production environment

## Important Configuration

Before running, update the following in docker-compose.yml:

- `APP_SECRET_TOKEN`: Change to a random secret token
- `SMTP_*` settings: Configure for email notifications
- `DOMAIN`: Set to your actual domain if not running locally

## Environment Variables

Key settings include:
- Database connection parameters
- SMTP configuration for email notifications
- Application domain and security settings

## Volumes

- `huginn-db`: MySQL database data

## Security Note

Make sure to change the `APP_SECRET_TOKEN` to a secure random value before deploying to production.

## License

MIT License