# WordPress Docker Compose

This is a complete WordPress setup with MySQL database using Docker Compose.

## Usage

1. **REQUIRED**: Change the placeholder passwords in `docker-compose.yml`:
   - Replace both instances of `CHANGE_ME_DB_PASSWORD` with your chosen password
   - Replace `CHANGE_ME_ROOT_PASSWORD` with your MySQL root password

2. Start the services:
   ```bash
   docker-compose up -d
   ```

3. Access WordPress at `http://localhost:8080` and complete the installation

## Stop the services

```bash
docker-compose down
```

To remove the data volumes as well:
```bash
docker-compose down -v
```

## What's included

- WordPress (latest version)
- MySQL 8.0 database
- Persistent data volumes for both WordPress and MySQL

## Security Note

**Important:** Change the default passwords before using in production!

## Customization

- Change the port mapping (8080:80) if port 8080 is already in use
- Modify environment variables for custom database credentials
