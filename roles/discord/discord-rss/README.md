# Discord.RSS

This is a role to facilitate the deployment of the Discord.RSS bot.
The deployment is made up of two parts:
- [Discord.RSS bot](./templates/deployment-bot.yml)
- [Discord.RSS web](./templates/deployment-web.yml)

While neither redis or mongodb are required, the application has to have some form of storage. An alternative (although recommended against) is using local storage /w hostpath.
For more information, read [the official docs](https://discordrss.xyz/).

Project repository: https://github.com/synzen/Discord.RSS-Clone

## Secrets
The secrets file (`vars/main.yml`) is expected to contain the following structure:

```yml
drss_secrets:
  discord_token: your-bot-token
  discord_client_id: your-app-client-id
  discord_client_secret: your-app-client-secret
  database:
    username: mongo-db-username
    password: mongo-db-password
```