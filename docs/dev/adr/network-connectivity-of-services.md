---
title: Network Connectivity of Services
parent: ADRs
last_modified_date: 5.6.2025
---

# Network Connectivity of Services
## Decision
We decided to use Docker Compose file to define a service name for each deployed service then it can be reused as the URL for other services in the same docker network although they are in separate repos and deployed separately.

### Option 1: Docker Compose

#### Pros
- We can simply use `http:://<service-name>:port` as the url if they are in same docker network
#### Cons
- network name in the compose file need to be maintained if it is different from `coolify`

### Option 2: Using consistent custom container name

#### Pros
- We can simply use `http:://<custom-container-name>:port` as the url if they are in same docker network
#### Cons
- We are losing the rolling update feature (continuous deployment without downtime)

### Option 3: No config -> use container name

#### Pros
- Simple
#### Cons
- Container name will change after each deployment
    - e.g. we need to update `telegram-interface` environment variable after each `linguly-core` update