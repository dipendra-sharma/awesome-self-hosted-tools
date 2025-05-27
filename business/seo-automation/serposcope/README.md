# Serposcope - Google Rank Tracking

Serposcope is a free rank tracker to monitor websites rankings in search engines and improve SEO.

## Features

- Track keyword rankings in Google
- Monitor multiple websites and keywords
- Historical ranking data
- Competitor analysis
- Scheduled rank checks
- Email notifications
- Export functionality

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Serposcope at http://localhost:8402

3. Create an account and start adding websites and keywords to track

## Configuration

- Port: 8402 (maps to internal port 7134)
- Database: MySQL 8.0
- Persistent data storage

## Database Configuration

The setup includes:
- MySQL database for storing ranking data
- Persistent volumes for data retention
- Environment variables for database connection

## Volumes

- `serposcope-db`: MySQL database data
- `serposcope-config`: Application configuration and data

## Notes

- First setup may take a few minutes to initialize the database
- Configure your keywords and tracking frequency in the web interface
- Be mindful of Google's rate limits when setting up frequent checks

## License

MIT License