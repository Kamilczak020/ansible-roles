# OAuth2 Proxy

This role facilitates the setup of an OAuth Proxy, to protect other services behind a login wall, when they do not feature their own authentication module.

The specific configuration and available ENV variables can be found at:
https://oauth2-proxy.github.io/oauth2-proxy/configuration

## Secrets
The secrets file (`vars/main.yml`) is expected to contain the following structure:

```yml
oauth_secrets:
  client-id: your-client-id
  client-secret: your-client-secret
  cookie-secret: your-cookie-secret
```