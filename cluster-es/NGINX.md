```bash
kubectl run nginx --image=nginx --restart=Never
kubectl run mycurlpod --image=curlimages/curl -i --tty -- sh
```


## Use Metricbeat to collect metrics

The following controllers can be used to deploy Metricbeat to the ACK cluster:

- DaemonSet: The DaemonSet controller ensures that each node in the cluster runs one pod. This enables Metricbeat to collect host metrics, system metrics, Docker statistics, and the metrics of all the services that are run on the ACK cluster.

- Deployment: You can use the Deployment controller to deploy a single Metricbeat shipper. The shipper is used to retrieve the unique metrics of the ACK cluster, such as metrics for Kubernetes events and the kube-state-metrics service.
