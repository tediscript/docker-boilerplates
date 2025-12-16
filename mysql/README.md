# MySQL Docker Compose

This is a MySQL 8.0 setup using Docker Compose.

## Usage

1. **REQUIRED**: Change the placeholder passwords in `docker-compose.yml`:
   - `MYSQL_ROOT_PASSWORD`: Root password for MySQL (replace CHANGE_ME_ROOT_PASSWORD)
   - `MYSQL_PASSWORD`: Password for the non-root user (replace CHANGE_ME_USER_PASSWORD)
   - Optionally modify:
     - `MYSQL_DATABASE`: Initial database to create
     - `MYSQL_USER`: Non-root user to create

2. Start the service:
   ```bash
   docker-compose up -d
   ```

3. Connect to MySQL:
   ```bash
   docker exec -it mysql mysql -u user -p
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

**Important:** Change the default passwords before using in production!
