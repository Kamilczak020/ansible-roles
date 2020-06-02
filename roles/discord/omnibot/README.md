# Omnibot

This is a role to prepare [Omnibot](https://gitlab.com/kamilczak020/omnibot) for deployment.
For more information, read the documentation in the project repo.

## Secrets
The secrets file (`vars/main.yml`) is expected to contain the following structure:

```yml
omnibot_secrets:
  discord_token: your-bot-token
  database_name: your-db-name
  database_host: your-db-host
  database_port: your-db-port
  database_username: your-db-username
  database_password: your-db-password
  oxford_app_id: oxford-api-app-id
  oxford_app_key: oxford-api-app-key
```