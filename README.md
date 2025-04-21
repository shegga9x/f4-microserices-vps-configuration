# Dockerized Microservices Setup

## Environment Variables
Common environment variables are stored in the `common.env` file.

## Running the application
To run the application with the environment variables:

```bash
docker-compose --env-file common.env up -d
```

This will load all environment variables from the common.env file and apply them to the services.

## Structure
- `docker-compose.yml`: Main configuration file that references service-specific configurations
- `common.env`: Common environment variables shared across services
- `docker/`: Contains service-specific configuration files
  - `base-service.yml`: Base configuration that all services extend
  - `apigateway.yml`: API Gateway specific configuration
  - `msmedia.yml`: Media service specific configuration
  - `msreels.yml`: Reels service specific configuration
  - `mysql.yml`: MySQL database configuration 