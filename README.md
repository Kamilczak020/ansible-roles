# Ansible Roles

A collection of useful ansible roles for setting up server things of all kinds.
These roles assume you are running Ubuntu but should work for most distributions, with possible minor changes required for the system setup and securing roles.

These roles assume your hosts are split into `masters` and `workers`. If that does not hold true, adjust `setup.yml` accordingly.

Featuring:
- [x] [Base system setup & configuration](./system)
- [x] [Installing and configuring Docker](./docker)
- [x] [Installing and configuring Kubernetes](./kubernetes)
- [x] [Networking utilities](./networking)
- [x] [Monitoring tools](./monitoring)
- [x] [Databases and their clusters](./database)
- [x] [Kafka cluster](./kafka)
- [x] [Specific Gitlab runners](./gitlab)
- [x] [Discord bots and applications](./discord)
- [x] [Scaleway CSI](./scaleway-csi)
- [x] [Personal blog deployment](./blog)