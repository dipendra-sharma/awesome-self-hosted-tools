# BookStack - Wiki-style Documentation System

BookStack is a simple, self-hosted, easy-to-use platform for organizing and storing information.

## Features

- Wiki-style documentation with books, chapters, and pages
- WYSIWYG editor with markdown support
- User roles and permissions
- Search functionality
- Dark and light themes
- Image management
- Multi-language support

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access BookStack at http://localhost:8400

3. Default login credentials:
   - Email: admin@admin.com
   - Password: password

## Configuration

- Port: 8400
- Database: MySQL 8.4
- Default timezone: UTC

## Environment Variables

Key configuration options can be modified in the docker-compose.yml file:

- `APP_URL`: The URL where BookStack will be accessible
- `TZ`: Timezone setting
- Database connection settings

## Volumes

- `bookstack-config`: Application configuration and data
- `bookstack-db`: MySQL database data

## License

MIT License