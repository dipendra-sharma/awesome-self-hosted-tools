# Nextcloud - File Sync and Collaboration Platform

Nextcloud is a self-hosted file sync and collaboration platform that gives you control over your data.

## Features

- File storage and synchronization
- Online office suite integration
- Calendar and contacts management
- Video and voice calls
- News and social feeds
- Task and project management
- Extensive app ecosystem
- End-to-end encryption

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Nextcloud at http://localhost:8518

3. Complete the setup with pre-configured admin credentials:
   - Username: admin
   - Password: admin123

## Configuration

- Port: 8518
- Database: PostgreSQL 16
- Redis caching enabled
- Admin credentials: admin/admin123 (change after first login)

## Services Included

- **nextcloud**: Main application server
- **nextcloud-db**: PostgreSQL database for data storage
- **nextcloud-redis**: Redis for caching and session storage

## Database Configuration

- Host: nextcloud-db
- Database: nextcloud
- Username: nextcloud
- Password: nextcloud_pass

## Volumes

- `nextcloud-db`: PostgreSQL database data
- `nextcloud-data`: Nextcloud files, apps, and configuration

## Initial Setup

1. Navigate to http://localhost:8518
2. Log in with admin/admin123
3. **Important**: Change the admin password immediately
4. Configure your instance settings
5. Install additional apps from the App Store

## Popular Apps

- **OnlyOffice**: Office suite integration
- **Calendar**: Calendar and scheduling
- **Contacts**: Contact management
- **Mail**: Email client
- **Talk**: Video calls and chat
- **News**: RSS/Atom feed reader
- **Tasks**: Task management

## Security Considerations

- Change default admin password immediately
- Use HTTPS in production
- Configure proper file permissions
- Regular backups of data and configuration
- Keep Nextcloud updated

## Client Applications

Download Nextcloud clients for:
- Desktop (Windows, macOS, Linux)
- Mobile (Android, iOS)
- WebDAV access for other applications

## Performance Optimization

This setup includes:
- PostgreSQL for better performance than SQLite
- Redis for caching and sessions
- Optimized for small to medium deployments

## License

AGPL v3