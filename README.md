# Docker Boilerplates

A collection of ready-to-use Docker Compose configurations for popular services and applications. These boilerplates help you quickly spin up development environments or deploy services with minimal configuration.

## Available Services

### Web Servers
- **[Nginx](./nginx/)** - High-performance web server and reverse proxy

### Databases
- **[MySQL](./mysql/)** - Popular relational database (MySQL 8.0)
- **[PostgreSQL](./postgresql/)** - Advanced relational database (PostgreSQL 15)
- **[MongoDB](./mongodb/)** - NoSQL document database (MongoDB 7)
- **[Redis](./redis/)** - In-memory data store and cache (Redis 7)

### CMS & Applications
- **[WordPress](./wordpress/)** - Complete WordPress setup with MySQL

## Quick Start

1. Navigate to the directory of the service you want to use:
   ```bash
   cd nginx
   ```

2. Start the service using Docker Compose:
   ```bash
   docker-compose up -d
   ```

3. Check the service-specific README.md for detailed usage instructions

4. Stop the service:
   ```bash
   docker-compose down
   ```

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed

## Usage Tips

- Each service directory contains:
  - `docker-compose.yml` - The Docker Compose configuration
  - `README.md` - Service-specific documentation and usage instructions

- Default configurations use common ports. Modify the port mappings if you have conflicts.

- For production use, **always change default passwords** and review security settings.

- Data is persisted using Docker volumes to survive container restarts.

## Customization

Feel free to modify the `docker-compose.yml` files to suit your needs:
- Change port mappings
- Adjust environment variables
- Add additional services
- Configure resource limits
- Set up networks for multi-service applications

## Contributing

Contributions are welcome! Feel free to submit pull requests with:
- New service boilerplates
- Improvements to existing configurations
- Better documentation
- Bug fixes

## License

MIT License - feel free to use these boilerplates in your projects.

## Security Notice

⚠️ **Warning**: These boilerplates use default credentials for ease of use in development. Always change passwords and review security settings before deploying to production environments.