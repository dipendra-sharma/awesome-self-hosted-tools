# Ghost - Modern Publishing Platform

Ghost is a modern, open-source publishing platform designed for content creators and bloggers.

## Features

- Clean, distraction-free writing interface
- Built-in SEO optimization
- Member subscriptions and payments
- Newsletter functionality
- Custom themes and design
- Fast performance
- Mobile-responsive admin interface
- Advanced analytics

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Ghost at http://localhost:8501

3. Complete the setup wizard to create your admin account

## Configuration

- Port: 8501 (maps to internal port 2368)
- Database: MariaDB 10.11
- Production environment

## Database Configuration

The setup includes MariaDB for better performance and reliability compared to SQLite.

## Environment Variables

Key settings include:
- Database connection parameters
- Site URL configuration
- Production environment settings

## Volumes

- `ghost-db`: MariaDB database data
- `ghost-content`: Ghost content including themes, images, and data

## Admin Setup

1. Navigate to http://localhost:8501/ghost
2. Create your admin account
3. Configure your publication settings
4. Start creating content

## Important Notes

- Uses MariaDB 10.11 to avoid MySQL 8.4 compatibility issues
- Default site URL is set to localhost:8501
- All Ghost features are available when self-hosting

## Content Management

- Write posts with the Ghost editor
- Organize content with tags
- Create custom pages
- Manage members and subscriptions
- Design your site with themes

## License

MIT License