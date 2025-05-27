# n8n - Visual Workflow Automation

n8n is a free and open fair-code licensed workflow automation tool.

## Features

- Visual workflow builder
- 300+ integrations
- Self-hosted solution
- Code execution capabilities
- Webhook support
- Scheduled workflows
- Error handling and retries

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access n8n at http://localhost:8404

3. Create an account and start building workflows

## Configuration

- Port: 8404 (maps to internal port 5678)
- Database: PostgreSQL 16
- Production environment

## Database

This setup uses PostgreSQL for better performance and reliability compared to the default SQLite database.

## Environment Variables

Key settings include:
- Database connection parameters
- Security and webhook configurations
- Timezone and environment settings

## Volumes

- `n8n-db`: PostgreSQL database data
- `n8n-data`: n8n application data including workflows and credentials

## Upgrading

To upgrade n8n, simply pull the latest image and restart:

```bash
docker compose pull
docker compose up -d
```

## License

Fair-code license (source-available)