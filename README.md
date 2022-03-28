# Docker dev-environnement

## Prerequisites
- mkcert: https://github.com/FiloSottile/mkcert
- docker & docker-compose

## Installation
### Get local ssl certificate
```
mkcert -install
mkcert -cert-file certs/local-cert.pem -key-file certs/local-key.pem "docker.localhost" "*.docker.localhost" "domain.local" "*.domain.local"

```

### Start the containers
```bash
docker-compose up -d
```
or you can start the containers one by one
```bash
docker-compose up -d [service_name]
```

## List of services

| Service     | Url                    |
|-------------|------------------------|
|reverse-proxy|-                       |
|phpmyadmin   |pma.docker.localhost    |
|adminer      |adminer.docker.localhost|
|mysql_5.6    |-                       |
|mysql_8.0    |-                       |
|mysql_5.7    |-                       |
|postgres_13  |-                       |