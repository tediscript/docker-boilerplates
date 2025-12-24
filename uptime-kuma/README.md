# uptime-kuma

Docker Compose configuration for Uptime Kuma, a self-hosted monitoring tool for uptime and status tracking.

## Quick Start

1. Navigate to the directory:
```bash
cd uptime-kuma
```

2. Start the service:
```bash
docker-compose up -d
```

3. Access Uptime Kuma at `http://localhost:3001`

4. Create an admin account on first launch

## Usage

```bash
# Start the service
docker-compose up -d

# Stop the service
docker-compose stop

# Restart the service
docker-compose restart

# View logs
docker-compose logs -f

# Stop and remove containers
docker-compose down
```

## Data Persistence

All monitoring data and configuration are stored in the `./data` directory.
