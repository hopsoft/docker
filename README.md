# Hopsoft Docker Images

Docker images for development and other environments.

## Quick Start

```sh
cd base
docker build -t hopsoft/base .
cd ../rails
cp .env.example .env
docker-compose build
```
