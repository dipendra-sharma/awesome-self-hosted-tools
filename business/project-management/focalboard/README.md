# Focalboard - Kanban-style Task Management

Focalboard is an open source, self-hosted alternative to Trello, Notion, and Asana.

## Features

- Kanban boards for task management
- Table and calendar views
- Real-time collaboration
- Template library
- Cards with rich content support
- Archive and restore functionality
- Export boards to various formats

## Quick Start

1. Run the service:
   ```bash
   docker compose up -d
   ```

2. Access Focalboard at http://localhost:8401

3. Create an account to get started

## Configuration

- Port: 8401 (maps to internal port 8000)
- Data persistence via Docker volume

## Environment Variables

- `VIRTUAL_HOST`: Virtual host configuration
- `VIRTUAL_PORT`: Internal port setting

## Volumes

- `focalboard-data`: Application data and boards

## Single Command Alternative

You can also run Focalboard with a single command:

```bash
docker run -d -p 8401:8000 --name focalboard mattermost/focalboard
```

## License

MIT License