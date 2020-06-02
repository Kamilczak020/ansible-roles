# MongoDB

This is a role to facilitate the creation of a mongodb cluster using a statefulset.
There are better, high-resilience options available, such as a [MongoDB Operator](https://docs.mongodb.com/kubernetes-operator/master/).

## Secrets
The secrets file (`vars/main.yml`) is expected to contain the following structure:

```yml
mongodb_secrets:
  keyfile: your-keyfile-hash
  username: your-superuser-username
  password: your-superuser-password
```

