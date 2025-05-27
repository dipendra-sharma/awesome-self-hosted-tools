# PostHog - Open-Source Product Analytics

PostHog is an open-source product analytics platform that helps you understand user behavior and improve your products.

## Features

- Event tracking and analytics
- User session recordings
- Feature flags and A/B testing
- Funnels and user journey analysis
- Cohort analysis
- Retention tracking
- Heatmaps and clickmaps
- Real-time dashboards

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Wait for all services to start (may take 2-3 minutes)

3. Access PostHog at http://localhost:8519

4. Create your account and organization

## Configuration

- Port: 8519
- Database: PostgreSQL 16 + ClickHouse for analytics
- Redis for caching and sessions

## Services Included

- **posthog**: Main application server
- **posthog-worker**: Background job processor
- **posthog-db**: PostgreSQL for application data
- **posthog-clickhouse**: ClickHouse for analytics data
- **posthog-redis**: Redis for caching

## Environment Variables

⚠️ **Important**: Change `SECRET_KEY` to a secure random value before production use.

Key settings include:
- Database connections
- ClickHouse configuration
- Site URL and security settings

## Volumes

- `posthog-db`: PostgreSQL application data
- `posthog-clickhouse`: ClickHouse analytics data
- `posthog-staticfiles`: Static files and assets

## Initial Setup

1. Navigate to http://localhost:8519
2. Create your PostHog account
3. Set up your organization
4. Install the PostHog snippet on your website
5. Start tracking events and analyzing user behavior

## Analytics Features

### Event Tracking
- Custom events and properties
- Automatic pageview tracking
- User identification
- Event filtering and segmentation

### User Insights
- User profiles and properties
- Session recordings
- User journey mapping
- Cohort analysis

### Product Features
- Feature flags for gradual rollouts
- A/B testing and experiments
- Funnel analysis
- Retention analysis

## Integration

Add PostHog to your website with the JavaScript snippet:

```javascript
!function(t,e){var o,n,p,r;e.__SV||(window.posthog=e,e._i=[],e.init=function(i,s,a){function g(t,e){var o=e.split(".");2==o.length&&(t=t[o[0]],e=o[1]);var n=t;return function(t){n[e]=t}}(p=t.createElement("script")).type="text/javascript",p.async=!0,p.src=s.api_host+"/static/array.js",(r=t.getElementsByTagName("script")[0]).parentNode.insertBefore(p,r);var u=e;for(void 0!==a?u=e[a]=[]:a="posthog",u.people=u.people||[],u.toString=function(t){var e="posthog";return"posthog"!==a&&(e+="."+a),t||(e+=" (stub)"),e},u.people.toString=function(){return u.toString(1)+".people (stub)"},o="capture identify alias people.set people.set_once set_config register register_once unregister opt_out_capturing has_opted_out_capturing opt_in_capturing reset isFeatureEnabled onFeatureFlags".split(" "),n=0;n<o.length;n++)g(u,o[n]);e._i.push([i,s,a])},e.__SV=1)}(document,window.posthog||[]);
posthog.init('YOUR_API_KEY',{api_host:'http://localhost:8519'})
```

## Security Notes

- Change the SECRET_KEY before production deployment
- Use HTTPS in production
- Configure proper CORS settings
- Secure ClickHouse and PostgreSQL access

## License

MIT License