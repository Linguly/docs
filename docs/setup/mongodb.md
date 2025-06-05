---
title: Mongodb for development or self-host
parent: Development Guide
nav_order: 3
last_modified_date: 5.6.2025
---
# Mongodb for development or self-host

For most of our functionalities we are using Mongodb primarily.
To have an easy local setup similar to the deployed version, we recommend to use the free tier of [MongoDB Atlas](https://www.mongodb.com/atlas).
There you can simply create an account [here](https://www.mongodb.com/atlas) and select the free tier.
Then create a connection url and update the `.env` file based on the Database instance you want to configure ([e.g. here in Linguly Core](https://github.com/Linguly/linguly-core?tab=readme-ov-file#environment-variables-for-local-setup)).
Create the DBs and collections as you need.


## Setup in Coolify

Mongodb setup in Coolify is straight forward:

- Create a new resource
- Select Mongodb and then Coolify will create a URL which include username and password
- Start the DB
- Copy the URL and paste it the mongodb url environment variable of the services you want e.g. [Linguly Core](https://github.com/Linguly/linguly-core)
