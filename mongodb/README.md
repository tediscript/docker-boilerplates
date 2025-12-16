# MongoDB Docker Compose

This is a MongoDB 7 setup using Docker Compose.

## Usage

1. **REQUIRED**: Change the placeholder password in `docker-compose.yml`:
   - `MONGO_INITDB_ROOT_PASSWORD`: Replace CHANGE_ME_PASSWORD with your chosen password
   - Optionally modify:
     - `MONGO_INITDB_ROOT_USERNAME`: Root username (default: admin)

2. Start the service:
   ```bash
   docker-compose up -d
   ```

3. Connect to MongoDB:
   ```bash
   docker exec -it mongodb mongosh -u admin -p
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

**Important:** Change the default credentials before using in production!

## Connection Details

- Host: localhost
- Port: 27017
- Username: admin (or as configured)
- Password: (as configured)

## Connection String

```
mongodb://admin:YOUR_PASSWORD@localhost:27017/
```
