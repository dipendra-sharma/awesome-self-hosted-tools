# Gitea - Lightweight Git Server

Gitea is a lightweight, self-hosted Git service that's easy to install and use.

## Features

- Git repository hosting
- Issue tracking
- Pull requests and code review
- Wiki for each repository
- Built-in CI/CD with Gitea Actions
- Package registry
- Project management
- User and organization management
- Lightweight and fast

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Gitea at http://localhost:8514

3. Complete the installation wizard

## Configuration

- Web Interface: Port 8514
- SSH: Port 8515
- Database: PostgreSQL 16

## Installation Wizard

On first access, you'll see the installation page:

1. **Database Settings**: Pre-configured for PostgreSQL
2. **General Settings**:
   - Site Title: Your choice
   - Repository Root Path: `/data/git/repositories`
   - Git LFS Root Path: `/data/git/lfs`
3. **Administrator Account**: Create your admin user

## Database Configuration

The setup uses PostgreSQL for better performance:
- Host: gitea-db:5432
- Database: gitea
- Username: gitea
- Password: gitea_pass

## Environment Variables

Key settings include:
- Database connection parameters
- Server domain and ports
- SSH configuration
- User registration settings

## Volumes

- `gitea-db`: PostgreSQL database data
- `gitea-data`: Git repositories and application data

## SSH Configuration

- SSH clone URLs will use port 8515
- Example: `git clone ssh://git@localhost:8515/username/repository.git`

## Git Operations

- HTTP clone: `git clone http://localhost:8514/username/repository.git`
- SSH clone: `git clone ssh://git@localhost:8515/username/repository.git`

## Features Setup

After installation, you can:
- Create organizations and teams
- Set up webhooks
- Configure Gitea Actions for CI/CD
- Enable package registries
- Create project boards

## Security

- Change default passwords in production
- Configure proper SSH keys
- Use HTTPS in production
- Regular updates and backups

## License

MIT License