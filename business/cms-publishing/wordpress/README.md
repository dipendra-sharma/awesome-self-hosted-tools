# WordPress - World's Most Popular CMS

WordPress is the world's most-used content management system and blogging platform, powering over 40% of all websites.

## Features

- User-friendly content management
- Thousands of themes and plugins
- SEO-friendly structure
- Multi-user support with roles and permissions
- Media library management
- Built-in commenting system
- Extensive customization options
- E-commerce capabilities with WooCommerce

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access WordPress at http://localhost:8500

3. Complete the WordPress installation wizard:
   - Choose your language
   - Create admin account
   - Configure site title and description

## Configuration

- Port: 8500
- Database: MariaDB 10.6.4
- Admin setup via web interface

## Database Configuration

- Host: wordpress-db
- Database: wordpress
- Username: wordpress
- Password: wordpress_pass

## Volumes

- `wordpress-db`: MariaDB database data
- `wordpress-data`: WordPress files, themes, plugins, and uploads

## Initial Setup

1. Navigate to http://localhost:8500
2. Select your language
3. Enter database connection details (already configured)
4. Create your admin account
5. Install themes and plugins as needed

## Security Notes

- Change default database passwords in production
- Use strong admin passwords
- Keep WordPress and plugins updated
- Consider security plugins for production use

## Popular Plugins

- Yoast SEO - Search engine optimization
- WooCommerce - E-commerce functionality
- Akismet - Spam protection
- Jetpack - Performance and security features

## License

GPL v2 or later