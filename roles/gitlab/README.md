# Gitlab Runners

This is a role to facilitate the deployment of gitlab runners.
This role can be adjusted to deploy runners for your own account, all it takes is to edit the statefulset and provide it with an appropriate Gitlab Token.

## Notes
Security could be greatly improved by adjusting the RBAC and assigning correct resources to the roles.