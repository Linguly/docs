---
title: Setup Ollama Connection
parent: Setup
---

# Setup Ollama Connection

One of the easiest way to host an open source model and connect to Linguly is to host a model from Ollama library in Coolify and connect to your Linguly Core via an Ollama Connection

## How to?

### 1. Download and Run a Model Using Ollama

1. Add ollama-with-open-webui in Coolify resources to a docker network same as your Linguly service.
1. Go to the terminal and connect to ollama api
1. Use the following command to download a desired model: `ollama pull llama3.2:3b`
    1. To check the result you can use `ollama list`
    1. If you want to run and test the model in terminal: `ollama run llama3.2:3b`
1. You can later remove the Open Webui by clicking on `Edit Compose File` and removing the section for Webui

### 2. Connect to your Linguly Core

In order to make a connection, we need to add the ollama service to the environment variables of our Linguly Core instance.

1. Modify the Compose file in Ollama service to add it to the same docker network as your Linguly Core.
  - For us its `coolify` network
  - The final compose file should look like this:

  ```
  services:
    ollama-api:
      image: 'ollama/ollama:latest'
      volumes:
        - 'ollama:/root/.ollama'
      networks:
        - coolify
      healthcheck:
        test:
          - CMD
          - ollama
          - list
        interval: 5s
        timeout: 30s
        retries: 10

  networks:
    coolify:
      external: true
  ```

2. In your Linguly Core instance, go to `Environment Variables` and then set `OLLAMA_URL` to `http://ollama-api:11434`

## For Local Tests  

You can install ollama locally from [here](https://ollama.com/download) and then `pull` a model similarly.
