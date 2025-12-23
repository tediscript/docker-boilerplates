# Cloudflare Tunnel

Docker Compose configuration for running a Cloudflare Tunnel (cloudflared) to securely expose your services.

## Quick Start

1. Create a tunnel in your [Cloudflare dashboard](https://one.dash.cloudflare.com/) and copy the tunnel token

2. Create a `.env` file with your tunnel token:
```bash
TUNNEL_TOKEN=your_tunnel_token_here
```

3. Start the tunnel:
```bash
docker-compose up -d
```

4. Verify it's running:
```bash
docker-compose logs -f
```

## Usage

```bash
# Start the tunnel
docker-compose up -d

# Stop the tunnel
docker-compose down

# View logs
docker-compose logs -f cloudflared

# Restart the tunnel
docker-compose restart
```
