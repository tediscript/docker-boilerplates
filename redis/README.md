# Redis Docker Compose

This is a Redis 7 setup using Docker Compose with data persistence enabled.

## Usage

1. Start the service:
   ```bash
   docker-compose up -d
   ```

2. Connect to Redis:
   ```bash
   docker exec -it redis redis-cli
   ```

## Stop the service

```bash
docker-compose down
```

To remove the data volume as well:
```bash
docker-compose down -v
```

## Features

- Redis 7 (Alpine-based for smaller image size)
- AOF (Append-Only File) persistence enabled
- Data volume for persistent storage

## Connection Details

- Host: localhost
- Port: 6379

## Security Note

For production use, consider:
- Adding password authentication (requirepass)
- Limiting network access
- Configuring proper persistence settings
