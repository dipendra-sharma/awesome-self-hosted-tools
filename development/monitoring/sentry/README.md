# Sentry Self-Hosted - Error Tracking & Performance Monitoring

Sentry is an open-source error tracking platform that helps developers monitor and fix crashes in real time.

## ⚠️ Important Notice

This is a **simplified configuration for testing purposes only**. For production deployment, please use the official Sentry self-hosted repository: https://github.com/getsentry/self-hosted

## Features

- **Error Tracking**: Real-time error monitoring and alerting
- **Performance Monitoring**: Application performance insights
- **Release Tracking**: Track deployments and their impact
- **Source Maps**: Debug minified code with source map support
- **Integrations**: Slack, GitHub, Jira, and 100+ integrations
- **Custom Dashboards**: Visualize errors and performance metrics
- **User Context**: Track user sessions and affected users

## Quick Start

1. **⚠️ Security First**: Change the `SENTRY_SECRET_KEY` in docker-compose.yml to a random 32+ character string

2. Run the service:
   ```bash
   docker compose up -d
   ```

3. Access Sentry at http://localhost:8632

4. Create your first user account and project

## Configuration

- **Port**: 8632 - Web interface
- **Database**: PostgreSQL 14 for application data
- **Cache**: Redis for session storage and caching
- **Workers**: Background job processing
- **Cron**: Scheduled task execution

## Production Setup

For production use, follow the official installation:

```bash
git clone https://github.com/getsentry/self-hosted.git
cd self-hosted
./install.sh
docker compose up -d
```

## Application Integration

### JavaScript/Node.js
```javascript
import * as Sentry from "@sentry/node";

Sentry.init({
  dsn: "YOUR_DSN_HERE",
  environment: "production",
});

// Capture an exception
try {
  throw new Error("Something went wrong");
} catch (e) {
  Sentry.captureException(e);
}
```

### Python
```python
import sentry_sdk

sentry_sdk.init(
    dsn="YOUR_DSN_HERE",
    environment="production",
)

# Capture an exception
try:
    1 / 0
except ZeroDivisionError:
    sentry_sdk.capture_exception()
```

### React
```jsx
import * as Sentry from "@sentry/react";

Sentry.init({
  dsn: "YOUR_DSN_HERE",
  environment: "production",
});

// Error Boundary
const SentryErrorBoundary = Sentry.withErrorBoundary(MyComponent, {
  fallback: ({ error }) => <div>Something went wrong: {error.message}</div>,
});
```

## Key Features

### Error Monitoring
- Real-time error alerts
- Stack trace analysis
- Error grouping and deduplication
- Custom fingerprinting

### Performance Monitoring
- Transaction tracking
- Database query monitoring
- HTTP request monitoring
- Custom instrumentation

### Release Management
- Deploy tracking
- Regression detection
- Commit and author tracking
- Issue assignment

## Services Architecture

- **Web**: Main application server
- **Worker**: Background job processing
- **Cron**: Scheduled tasks (cleanup, digests)
- **PostgreSQL**: Primary data storage
- **Redis**: Caching and queue management

## Security Considerations

- Change default secret keys before production
- Use HTTPS in production
- Configure proper authentication (SAML/SSO available)
- Set up proper network security
- Regular backups of PostgreSQL data

## Supported Languages

- JavaScript/TypeScript
- Python
- PHP
- Ruby
- Java
- C#/.NET
- Go
- Rust
- And 30+ more languages

## License

Functional Source License (FSL-1.1-Apache-2.0)