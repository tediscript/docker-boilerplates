# PostgreSQL Docker Compose

This is a PostgreSQL 15 setup using Docker Compose.

## Usage

1. (Optional) Modify the environment variables in `docker-compose.yml`:
   - `POSTGRES_USER`: Database user (default: postgres)
   - `POSTGRES_PASSWORD`: Database password
   - `POSTGRES_DB`: Initial database to create

2. Start the service:
   ```bash
   docker-compose up -d
   ```

3. Connect to PostgreSQL:
   ```bash
   docker exec -it postgresql psql -U postgres
   ```

## Stop the service

```bash
docker-compose down
```

To remove the data volume as well:
```bash
docker-compose down -v
```

## Security Note

**Important:** Change the default password before using in production!

## Connection Details

- Host: localhost
- Port: 5432
- User: postgres (or as configured)
- Database: mydb (or as configured)
