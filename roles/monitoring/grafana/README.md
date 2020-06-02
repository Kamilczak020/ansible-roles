# Grafana

This is a role to facilitate the deployment of Grafana.
You can configure specifics using `defaults/main.yml`.

## Notes
This role deploys Grafana on a `/grafana` subpath.
If you wish to not use the subpath, adjust the [Ingress](./templates/ingress.j2) and the `GF_SERVER_ROOT_URL` container ENV variable in the [deployment](./templates/deployment.j2).