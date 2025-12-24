# Redis

A high-performance in-memory data structure store used as a database, cache, and message broker.

## Quick Start

1. Create a `.env` file:
```bash
cp .env.example .env
```

2. Set a strong password in `.env`:
```
REDIS_PASSWORD=your_secure_password
```

3. Start the service:
```bash
docker compose up -d
```

## Usage

Start the service:
```bash
docker compose start
```

Stop the service:
```bash
docker compose stop
```

View logs:
```bash
docker compose logs -f
```

Restart the service:
```bash
docker compose restart
```

Access redis-cli:
```bash
docker exec -it redis redis-cli -a your_password
```

## Configuration

Redis is accessible at `localhost:6379` with password authentication enabled.

Connection string format:
```
redis://:your_password@localhost:6379
```

This setup uses Redis 7.2.5, a stable version chosen to avoid issues present in Redis 7.4.x releases.

## Data Persistence

Redis data is persisted in the `./data` directory, which stores RDB snapshots and AOF logs.
