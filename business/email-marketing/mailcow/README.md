# Mailcow - Complete Email Server Solution

Mailcow is a dockerized email server solution providing a complete mail infrastructure with web interface.

## ⚠️ Important Notice

This is a **simplified configuration for testing purposes only**. For production deployment, please use the official mailcow-dockerized repository which includes all necessary components and security configurations.

## Features

- Complete email server (SMTP, IMAP, POP3)
- Web-based administration interface
- Spam filtering and antivirus
- DKIM signing and verification
- Webmail interface
- Two-factor authentication
- SSL/TLS encryption
- Backup and restore functionality

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access the web interface at http://localhost:8509

3. Configure your domain and SSL certificates

## Configuration

- Web Interface: Port 8509 (HTTP), 8510 (HTTPS)
- SMTP: Port 8502 (25), 8503 (587), 8504 (465)
- IMAP: Port 8505 (143), 8506 (993)
- POP3: Port 8507 (110), 8508 (995)

## Services Included

- **mailcow-postfix**: SMTP server for sending/receiving emails
- **mailcow-dovecot**: IMAP/POP3 server for email access
- **mailcow-web**: Web interface for administration
- **mailcow-mariadb**: Database for configuration storage
- **mailcow-redis**: Caching and session storage

## Production Deployment

For production use:

1. Clone the official repository:
   ```bash
   git clone https://github.com/mailcow/mailcow-dockerized
   cd mailcow-dockerized
   ```

2. Generate configuration:
   ```bash
   ./generate_config.sh
   ```

3. Customize mailcow.conf for your domain

4. Start the services:
   ```bash
   docker compose up -d
   ```

## Security Considerations

- Use proper SSL certificates in production
- Configure SPF, DKIM, and DMARC records
- Set up proper firewall rules
- Regular security updates
- Strong passwords for all accounts

## Domain Configuration

Before production use, configure:
- MX records pointing to your server
- SPF record for sender verification
- DKIM keys for email signing
- DMARC policy for email authentication

## License

GPL v3