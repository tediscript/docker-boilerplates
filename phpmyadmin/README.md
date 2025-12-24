# phpMyAdmin

A web-based database management tool for MySQL and MariaDB servers.

## Quick Start

1. Start the service:
```bash
docker compose up -d
```

2. Access phpMyAdmin at http://localhost

3. Enter your MySQL/MariaDB server details to connect

## Usage

Start the service:
```bash
docker compose up -d
```

Stop the service:
```bash
docker compose down
```

View logs:
```bash
docker compose logs -f
```

Restart the service:
```bash
docker compose restart
```

## Configuration

- **Arbitrary Server Mode**: Enabled (`PMA_ARBITRARY=1`) - allows connecting to any MySQL/MariaDB server
- **Upload Limit**: 2GB maximum file upload size
- **Memory Limit**: 4GB PHP memory limit
- **Max Execution Time**: 36000 seconds (10 hours)
- **Cookie Expiration**: 24 hours

## Logs

Apache logs are stored in the `./log` directory.
