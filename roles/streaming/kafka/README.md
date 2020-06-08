# Kafka Role

This role is based on [Yolean/kubernetes-kafka](https://github.com/Yolean/kubernetes-kafka). The aim of this role is to set up a production-ready kafka cluster on kubernetes.

### Volumes
This role assumes you have servers on scaleway, as it uses scaleway-csi's storage class `scw-bssd` to provision volumes.
If that is not the case, edit `storageClassName` (zookeeper/zoo.yml, zookeeper/pzoo.yml, kafka/statefulset.yml) to match the name of your storage class used for volume provisioning. You can also adjust volume sizes there.