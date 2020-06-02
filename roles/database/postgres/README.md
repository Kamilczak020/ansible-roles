# Postgres

This is a role to facilitate deployment of a postgres container using a statefulset.
This is a low-resource, but also a low resilience solution.

For a high resilience solution, refer to [Postgres Cluster Role](../postgres-cluster).

## Secrets
The secrets file (`vars/main.yml`) is expected to contain the following structure:

```yml
postgres_secrets:
  db: your-database-name
  user: your-superuser-username
  password: your-superuser-password
```

