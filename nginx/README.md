# nginx

## Description

This is a Docker Compose configuration for running nginx as a web server or reverse proxy. It works out-of-the-box with a hello world page and uses nginx's default configuration with optional custom server blocks.

## Overview

nginx is a high-performance HTTP server and reverse proxy. This Docker Compose setup provides a quick way to deploy nginx in a containerized environment without touching the main `nginx.conf` file.

## Features

- ✅ **Works immediately** - Includes a hello world page
- 🔧 **Hook-based configuration** - Add custom server blocks in `conf.d/` without modifying main nginx.conf
- 🔒 **SSL ready** - Example configurations for HTTPS setup
- 🔄 **Reverse proxy examples** - Ready-to-use proxy configurations
- 📦 **Clean structure** - Organized directories for content, configs, and certificates

## Quick Start

1. Clone or copy this directory to your project
2. Run `docker-compose up -d`
3. Open http://localhost in your browser
4. You should see the hello world page!

## Directory Structure

```
.
├── docker-compose.yml
├── .gitignore
├── html/
│   └── index.html              # Your web content (hello world included)
├── conf.d/
│   ├── default.conf.example    # Basic HTTP server config
│   ├── reverse-proxy.conf.example  # Reverse proxy setup
│   └── ssl.conf.example        # HTTPS/SSL configuration
└── ssl/                        # SSL certificates (add your own)
```

## Configuration

### Using Default Setup

The setup works immediately with nginx's default configuration. Just add your HTML files to the `html/` directory.

### Adding Custom Server Blocks

To add custom configurations, copy one of the example files and modify it:

```bash
# Basic HTTP server
cp conf.d/default.conf.example conf.d/default.conf

# Reverse proxy
cp conf.d/reverse-proxy.conf.example conf.d/reverse-proxy.conf

# SSL/HTTPS
cp conf.d/ssl.conf.example conf.d/ssl.conf
```

Edit the `.conf` file with your settings (server name, proxy targets, etc.), then reload nginx:

```bash
docker-compose exec nginx nginx -s reload
```

### Volumes

The following directories are mounted:
- `./html:/usr/share/nginx/html` - Static web content
- `./conf.d:/etc/nginx/conf.d` - Custom server block configurations
- `./ssl:/etc/nginx/ssl` - SSL certificates and keys

### Ports

- **80** - HTTP
- **443** - HTTPS (configure SSL in conf.d/)

## Usage

### Start the service
```bash
docker-compose up -d
```

### Stop the service
```bash
docker-compose down
```

### View logs
```bash
docker-compose logs -f nginx
```

### Reload configuration without downtime
```bash
docker-compose exec nginx nginx -s reload
```

### Test configuration
```bash
docker-compose exec nginx nginx -t
```

## Examples

### Basic Static Website

Just add your HTML, CSS, and JS files to the `html/` directory. They'll be served automatically.

### Reverse Proxy

1. Copy the reverse proxy example:
   ```bash
   cp conf.d/reverse-proxy.conf.example conf.d/reverse-proxy.conf
   ```

2. Edit `conf.d/reverse-proxy.conf` and update:
   - `server_name` to your domain
   - `proxy_pass` to your backend service URL

3. Reload nginx:
   ```bash
   docker-compose exec nginx nginx -s reload
   ```

### HTTPS/SSL Setup

1. Place your SSL certificate files in the `ssl/` directory:
   - `ssl/certificate.crt`
   - `ssl/private.key`

2. Copy and configure the SSL example:
   ```bash
   cp conf.d/ssl.conf.example conf.d/ssl.conf
   ```

3. Edit `conf.d/ssl.conf` and update the paths and server name

4. Reload nginx:
   ```bash
   docker-compose exec nginx nginx -s reload
   ```

## Notes

- The main `nginx.conf` is not modified - we use the default nginx configuration
- Custom server blocks in `conf.d/*.conf` are automatically included
- Example files (`*.conf.example`) are safe to keep and won't be loaded by nginx
- SSL certificates are gitignored for security