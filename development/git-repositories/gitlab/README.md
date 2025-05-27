# GitLab - Complete DevOps Platform

GitLab is a complete DevOps platform providing Git repository management, CI/CD, and more in a single application.

## Features

- Git repository hosting
- Issue tracking and project management
- Continuous Integration/Continuous Deployment (CI/CD)
- Container registry
- Wiki and documentation
- Code review with merge requests
- Security scanning
- Monitoring and analytics

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Wait for GitLab to start (may take 2-3 minutes)

3. Access GitLab at http://localhost:8511

4. Get the initial root password:
   ```bash
   docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
   ```

## Configuration

- Web Interface: Port 8511 (HTTP), 8512 (HTTPS)
- SSH: Port 8513
- Default user: root
- Password: Retrieved from container (see Quick Start step 4)

## Important Notes

- First startup takes several minutes to initialize
- GitLab is configured for reduced memory usage
- SSH clone URLs will use port 8513
- Default external URL is set to localhost:8511

## Memory Configuration

This configuration includes optimizations for smaller deployments:
- Reduced PostgreSQL shared buffers
- Limited worker processes
- Lower memory limits for Unicorn workers

## Initial Setup

1. Navigate to http://localhost:8511
2. Log in with username `root` and the password from the container
3. Change the root password
4. Create your first project or import existing repositories
5. Configure CI/CD pipelines as needed

## Git Operations

- HTTP clone: `git clone http://localhost:8511/username/repository.git`
- SSH clone: `git clone ssh://git@localhost:8513/username/repository.git`

## Volumes

- `gitlab-config`: GitLab configuration files
- `gitlab-logs`: Application logs
- `gitlab-data`: Git repositories and application data

## Production Considerations

For production deployment:
- Use proper domain name and SSL certificates
- Increase memory limits based on usage
- Configure backup strategies
- Set up email notifications
- Configure external database for better performance

## License

MIT License (Community Edition)