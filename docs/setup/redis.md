---
title: Redis for development or self-host
parent: Development Guide
nav_order: 4
last_modified_date: 5.6.2025
---
# Redis for development or self-host

For most of our in memory DB usages we are using Redis primarily.
To have an easy local setup just install it locally and make sure it is running when you are running any service depending on it e.g. [Telegram Interface](https://github.com/Linguly/telegram-interface).

## Setup in Coolify

Redis setup in Coolify is straight forward:
- Create a new resource
- Select Redis and then Coolify will create a URL and a password
- Start the DB
- Copy the URL and Password, and paste them to the respective environment variables of the services you want e.g. [Telegram Interface](https://github.com/Linguly/telegram-interface).
