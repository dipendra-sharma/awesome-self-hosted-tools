# Umami - Privacy-Focused Web Analytics

Umami is a simple, fast, privacy-focused alternative to Google Analytics that respects user privacy.

## Features

- Privacy-focused analytics
- No cookies or personal data collection
- Real-time website statistics
- Custom events tracking
- Multiple website support
- Lightweight tracking script
- Simple and clean interface
- GDPR compliant

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Wait for the database to initialize

3. Access Umami at http://localhost:8520

4. Login with default credentials:
   - Username: admin
   - Password: umami

## Configuration

- Port: 8520 (maps to internal port 3000)
- Database: PostgreSQL 16
- Health checks enabled for reliability

## Environment Variables

⚠️ **Important**: Change `APP_SECRET` to a secure random value before production use.

Key settings include:
- Database connection URL
- Application secret for security
- Hostname configuration

## Volumes

- `umami-db`: PostgreSQL database for analytics data

## Initial Setup

1. Navigate to http://localhost:8520
2. Log in with admin/umami
3. **Important**: Change the admin password immediately
4. Add your first website:
   - Go to Settings > Websites
   - Click "Add website"
   - Enter your website URL and name
5. Copy the tracking code to your website

## Adding Tracking Code

After adding a website, you'll get a tracking script like:

```html
<script async src="http://localhost:8520/script.js" data-website-id="your-website-id"></script>
```

Add this to the `<head>` section of your website.

## Analytics Features

### Basic Analytics
- Page views and unique visitors
- Bounce rate and session duration
- Top pages and referrers
- Country and device information

### Advanced Features
- Custom event tracking
- Goal conversion tracking
- Real-time visitor monitoring
- Historical data analysis

### Privacy Features
- No cookies used
- No personal data collected
- IP addresses are anonymized
- GDPR compliant by design

## Custom Events

Track custom events with JavaScript:

```javascript
// Track a custom event
umami.track('button-click', { button: 'header-cta' });

// Track with custom properties
umami.track('purchase', { 
  value: 99.99, 
  currency: 'USD' 
});
```

## Security Considerations

- Change default admin password immediately
- Use strong password for admin account
- Change APP_SECRET to a random value
- Use HTTPS in production
- Regular backups of analytics data

## Multi-Website Support

Umami supports tracking multiple websites from a single installation:
- Each website gets a unique tracking ID
- Separate analytics for each domain
- Centralized management interface

## Performance

- Lightweight tracking script (<2KB)
- Fast loading times
- Minimal impact on website performance
- Real-time data processing

## License

MIT License