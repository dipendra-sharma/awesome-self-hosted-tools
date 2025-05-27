# Socioboard - Social Media Management

Socioboard is an open source social technology enabler for scheduling and managing social media posts.

## Features

- Schedule posts across multiple social platforms
- Social media analytics
- Team collaboration
- Content calendar
- Bulk scheduling
- Social listening
- Multi-account management

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Socioboard at http://localhost:8405

3. Create an account and connect your social media accounts

## Configuration

- Port: 8405
- Database: MySQL 8.0
- Redis for caching
- Development mode (default)

## Important Security Notes

⚠️ **Security Warning**: This configuration runs in development mode with debugging enabled. Do not expose this application to the internet without proper security configuration.

## Environment Variables

Update the following secrets in docker-compose.yml:
- `SESSION_SECRET`: Change to a random secret
- `JWT_SECRET`: Change to a random JWT secret

## Services

- **socioboard**: Main application
- **socioboard-db**: MySQL database
- **socioboard-redis**: Redis cache

## Volumes

- `socioboard-db`: MySQL database data
- `socioboard-data`: Application uploads and data

## Production Deployment

For production use:
1. Change `NODE_ENV` to `production`
2. Update security configurations
3. Use proper SSL/TLS setup
4. Configure environment secrets securely

## License

GPL v3