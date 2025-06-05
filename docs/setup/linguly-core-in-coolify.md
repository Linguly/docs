---
title: Setup Linguly Core in Coolify
parent: Setup
nav_order: 2
---

# Setup Linguly Core in Coolify

## Docker Network
- Setup it in same network as other services
- Setup in `coolify` default network otherwise need to modify network in the docker-compose.yaml
- More info in [this ADR](../dev/adr/network-connectivity-of-services.md)

## Environment Variables
Add the environment variables based on the [readme](https://github.com/Linguly/linguly-core?tab=readme-ov-file#environment-variables-for-local-setup).

