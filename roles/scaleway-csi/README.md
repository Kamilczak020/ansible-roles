## Scaleway CSI

This role sets up scaleway-csi on your kubernetes cluster.

As of today (2020-04-09), it features a workaround for https://github.com/scaleway/scaleway-csi/issues/13, where kube won't recognize in-file CRD, so we apply it separately before applying the manifest.