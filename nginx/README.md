# Nginx Docker Compose

This is a basic Nginx setup using Docker Compose.

## Usage

1. Create an `html` directory to serve your static files:
   ```bash
   mkdir html
   echo "<h1>Hello from Nginx</h1>" > html/index.html
   ```

2. (Optional) Create a custom `nginx.conf` file and uncomment the volume mount in `docker-compose.yml`

3. Start the service:
   ```bash
   docker-compose up -d
   ```

4. Access the service at `http://localhost`

## Stop the service

```bash
docker-compose down
```

## Customization

- Modify the ports in the `docker-compose.yml` file if needed
- Add SSL certificates in volumes for HTTPS support
- Customize `nginx.conf` for advanced configurations
