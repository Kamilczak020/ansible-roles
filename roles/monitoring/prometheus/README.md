## Prometheus Role

This role creates a prometheus deployment, and exposes it outside the cluster through nginx-ingress.

To run this role, you will need a `vars/main.yml`(perferably vaulted), that contains following keys:

```yml
prometheus_auth:
  username: panel-username
  password: panel-password
```

The above are used for setting up basic auth for the (usually unprotected) prometheus dashboard.

### Notes
Currently, this uses `htpasswd` to generate the auth string (and does so on the target). Make sure that it is available on the system. If you'd rather generate those on your ansible controller host, you will need to edit the tasks to delegate the work (and tasks).

Letting go of `htpasswd` is possible in the future, as long as ansible supports apache-recognizable password hashing formats in their filters.