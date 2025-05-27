# Zammad - Open Source Help Desk

Zammad is a web-based, open-source user support/ticketing solution with many features to manage customer communications.

## Features

- **Multi-Channel Support**: Email, phone, chat, social media, and web forms
- **Knowledge Base**: Self-service documentation and FAQ system
- **Ticket Management**: Advanced ticket routing, escalation, and SLA management
- **Team Collaboration**: Internal notes, ticket assignment, and team communication
- **Reporting & Analytics**: Comprehensive reporting and dashboard views
- **Automation**: Triggers, schedulers, and macros for workflow automation
- **Mobile Support**: Responsive web interface and mobile apps
- **Integrations**: API access and third-party integrations

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Wait for all services to initialize (may take 3-5 minutes)

3. Access Zammad at http://localhost:8641

4. Complete the initial setup wizard

## Configuration

- **Port**: 8641 - Web interface
- **Database**: PostgreSQL 15 for application data
- **Search**: Elasticsearch 8.8.1 for full-text search
- **Cache**: Memcached for session caching
- **Queue**: Redis for background job processing

## Services Architecture

- **Rails Server**: Main web application
- **Scheduler**: Background job processing and automation
- **WebSocket**: Real-time updates and notifications
- **PostgreSQL**: Primary database
- **Elasticsearch**: Search and indexing
- **Memcached**: Session and object caching
- **Redis**: Queue management

## Initial Setup

1. **Admin Account**: Create your admin account during first access
2. **Email Configuration**: Configure SMTP settings for email notifications
3. **Channels**: Set up email channels, web forms, or integrations
4. **User Management**: Create agents and customer accounts
5. **Groups & Roles**: Configure permissions and access levels

## Key Features

### Ticket Management
- Automatic ticket creation from multiple channels
- Ticket routing based on content and rules
- SLA management with escalation policies
- Merge, split, and link related tickets

### Knowledge Base
- Create articles and categories
- Multi-language support
- Search integration with Elasticsearch
- Public and internal articles

### Automation
- **Triggers**: Automatic actions based on ticket changes
- **Schedulers**: Time-based actions and escalations
- **Macros**: Bulk operations and quick actions
- **Auto-Assignment**: Intelligent ticket routing

### Reporting
- Dashboard with key metrics
- Custom reports and analytics
- Performance tracking for agents
- Customer satisfaction surveys

## Email Integration

### Inbound Email
```
Configure email channels to automatically create tickets:
- POP3/IMAP mailbox monitoring
- Email forwarding setup
- API-based email integration
```

### Outbound Email
```
SMTP configuration for notifications:
- Ticket updates and responses
- Agent notifications
- Customer communications
```

## API Usage

Zammad provides a comprehensive REST API:

```bash
# Get tickets
curl -H "Authorization: Token YOUR_API_TOKEN" \
  http://localhost:8641/api/v1/tickets

# Create ticket
curl -X POST -H "Authorization: Token YOUR_API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"title":"Test Ticket","customer_id":1,"group_id":1}' \
  http://localhost:8641/api/v1/tickets
```

## Integrations

### Popular Integrations
- **Slack**: Ticket notifications and updates
- **GitHub**: Link tickets to issues and PRs
- **LDAP/AD**: User authentication and sync
- **Monitoring**: Create tickets from monitoring alerts

### Custom Integrations
- REST API for custom applications
- Webhook support for real-time events
- OAuth2 authentication

## Mobile Access

- Responsive web interface works on mobile devices
- Native mobile apps available for iOS and Android
- Real-time notifications and updates

## Customization

### Themes and Branding
- Custom CSS and themes
- Logo and color scheme customization
- White-label options

### Custom Fields
- Add custom fields to tickets and users
- Configure field types and validations
- Use in automation and reporting

## Performance Optimization

### Elasticsearch
- Ensure adequate memory allocation (1GB+ recommended)
- Monitor search performance and indexing
- Configure proper cluster settings for production

### Database
- Regular PostgreSQL maintenance and optimization
- Configure appropriate connection pooling
- Monitor query performance

### Caching
- Memcached configuration for optimal performance
- Redis tuning for background jobs
- Static asset caching strategies

## Security Considerations

- **Authentication**: Configure secure authentication methods
- **HTTPS**: Use SSL/TLS in production
- **Permissions**: Set up proper role-based access
- **API Security**: Secure API tokens and endpoints
- **Data Privacy**: GDPR compliance features available

## Backup Strategy

- Regular PostgreSQL database backups
- Elasticsearch index backups
- File storage and attachment backups
- Configuration file backups

## Production Requirements

- **Minimum**: 4GB RAM, 2 CPU cores
- **Recommended**: 8GB+ RAM, 4+ CPU cores
- **Storage**: SSD recommended for database and search
- **Network**: Proper firewall and security group configuration

## License

AGPL v3 (Open Source)