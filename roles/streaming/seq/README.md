# Seq Role

This role facilitates deployment of Seq, a logging solution by Datalust.
For details, refer here:
https://docs.datalust.co/docs/getting-started-with-docker

Seq runs an API by default on port `80`, and an ingest endpoint on port `5431`.

By default, the seq pod is given 1Gi of memory.
If you would like to change that value, edit the `StatefulSet` accordingly.