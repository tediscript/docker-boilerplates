# nginx

Docker Compose configuration for running nginx as a web server or reverse proxy with optional custom server blocks.

## Quick Start

1. Run the container:
```bash
docker-compose up -d
```

2. Open http://localhost in your browser to see the hello world page

3. (Optional) Add custom configurations by copying example files:
```bash
cp conf.d/default.conf.example conf.d/default.conf
cp conf.d/reverse-proxy.conf.example conf.d/reverse-proxy.conf
cp conf.d/ssl.conf.example conf.d/ssl.conf
```

4. Reload nginx after config changes:
```bash
docker-compose exec nginx nginx -s reload
```

## Usage

```bash
# Start the service
docker-compose up -d

# Stop the service
docker-compose down

# View logs
docker-compose logs -f nginx

# Test configuration
docker-compose exec nginx nginx -t

# Reload configuration
docker-compose exec nginx nginx -s reload
```

## Directories

- `html/` - Static web content (served at http://localhost)
- `conf.d/` - Custom server block configurations
- `ssl/` - SSL certificates and keys