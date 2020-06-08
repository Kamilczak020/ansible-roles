# Ansible Roles

A collection of useful ansible roles for setting up server things of all kinds.
These roles assume you are running Ubuntu but should work for most distributions, with possible minor changes required for the system setup and securing roles.

Many of the roles are highly configurable through data in `defaults` and `vars`. For specific use-cases, you will have to edit the manifests.

### Note

These roles assume your hosts are split into `masters` and `workers`. If that does not hold true, adjust `setup.yml` accordingly.

## Table of contents
- [Base system setup & configuration](./roles/system)
  - [Configure System](./roles/system/config-system)
  - [Secure System](./roles/system/secure-system)
  - [Install openshift](./roles/system/openshift)
- [Installing and configuring Docker](./roles/docker)
- [Installing and configuring Kubernetes](./roles/kubernetes)
  - [Master Nodes](./roles/kubernetes/masters)
  - [Worker Nodes](./roles/kubernetes/workers)
- [Networking utilities](./roles/networking)
  - [Nginx Ingress](./roles/networking/nginx-ingress)
  - [Letsencrypt Cert Manager](./roles/networking/cert-manager)
  - [Peervpn](./roles/networking/peervpn)
- [Monitoring tools](./roles/monitoring)
  - [Prometheus](./roles/monitoring/prometheus)
  - [Prometheus Kafka Plugin](./roles/monitoring/prometheus-kafka)
  - [Kube State Metrics](./roles/monitoring/kube-state-metrics)
  - [Grafana](./roles/monitoring/grafana)
- [Security tools](./roles/security)
  - [OAuth2 Proxy](./roles/security/oauth2-proxy)
- [Databases and their clusters](./roles/database)
  - [Postgres](./roles/database/postgres)
  - [Postgres Cluster + Operator](./roles/database/postgres-cluster)
  - [Redis](./roles/database/redis)
  - [Mongodb Cluster](./roles/database/mongodb)
- [Streaming tools](./roles/streaming)
  - [Kafka cluster](./roles/streaming/kafka)
  - [Seq](./roles/streaming/seq)
- [Specific Gitlab runners](./roles/gitlab)
- [Discord bots and applications](./roles/discord)
  - [Discord RSS](./roles/discord/discord-rss)
  - [Omnibot](./roles/discord/omnibot)
- [Scaleway CSI](./roles/scaleway-csi)
- [Personal blog deployment](./roles/blog)

## How to use

1. Clone the repository: 
```
git clone https://github.com/Kamilczak020/ansible-roles.git
```

2. Adjust `group_vars` and specific role variables using `ansible-vault`.

3. Run a specific playbook using it's tag:
```
ansible-playbook setup.yml --tags=your-tags-here --ask-vault-password
```