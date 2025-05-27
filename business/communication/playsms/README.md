# PlaySMS - Bulk SMS Campaigns

PlaySMS is a web interface for SMS gateways and bulk SMS services.

## Features

- Send bulk SMS campaigns
- SMS gateway integration
- User management
- SMS templates
- Delivery reports
- Credit management
- API support
- Multiple gateway support

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access PlaySMS at http://localhost:8407

3. Login with default credentials:
   - Username: admin
   - Password: admin

## Configuration

- Port: 8407
- Database: MySQL 8.0
- Default admin credentials (change after first login)

## Important Security Note

⚠️ **Security**: Change the default admin password immediately after first login. PlaySMS version 1.4.6 contains critical security fixes.

## SMS Gateway Configuration

After installation, configure your SMS gateway in the admin panel:
- Go to Admin → Manage gateway
- Add your SMS provider settings
- Configure SMS routes and pricing

## Environment Variables

- Database connection settings
- Admin user credentials
- Application title configuration

## Volumes

- `playsms-db`: MySQL database data
- `playsms-data`: Application storage
- `playsms-logs`: Application logs

## API Usage

PlaySMS provides a web service API for:
- Sending SMS messages
- Checking delivery status
- Managing contacts and groups

## License

GPL v3