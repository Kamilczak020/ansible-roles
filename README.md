# Ansible Roles

A collection of useful ansible roles for setting up server things of all kinds.
These roles assume you are running Ubuntu but should work for most distributions, with possible minor changes required for the system setup and securing roles.

These roles assume your hosts are split into `masters` and `workers`. If that does not hold true, adjust `setup.yml` accordingly.

Featuring:
- [x] Base server setup [config_system]
- [x] Securing the system [secure_system]
- [x] Installing and configuring Docker, using docker-ce [docker]
- [x] Installing openshift
- [x] Setting up Kubernetes cluster and control plane [kubernetes/masters]
- [x] Joining kubernetes cluster from workers [kubernetes/workers]
- [x] Deploying Gitlab specific runners [gitlab]
- [x] Setting up prometheus for tracking Kubernetes stats [monitoring/prometheus]
- [x] More metrics through `kube-state-metrics` [monitoring/kube-state-metrics]
- [x] A grafana dashboard for monitoring [monitoring/grafana]