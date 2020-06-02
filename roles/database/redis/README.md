# Redis Cluster

This is a role to facilitate the creation of a redis cluster.
While the deployment of all the manifests is automatic, there is manual action required to initialize the cluster itself.

This role is based on:
https://github.com/rustudorcalin/deploying-redis-cluster

## Deployment

After running the role, you need to form the cluster.
This can be done by executing a `redis-cli` command inside the master instance.

Note: If you changed the namespace in `defaults`, make sure to reflect that change in the command.
```bash
kubectl exec -it redis-cluster-0 -n redis -- redis-cli --cluster create --cluster-replicas 1 $(kubectl get pods -l app=redis-cluster -o jsonpath='{range.items[*]}{.status.podIP}:6379 ')
```

## Notes
Bear in mind, that while you can scale up the number of pods in the cluster, the minimum required by redis is 6.
If you wish to include a [Pod Affinity](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/) to improve resilience, make sure you have the required amount of untainted nodes.