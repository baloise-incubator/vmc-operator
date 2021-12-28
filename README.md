# Virtual Machine Cluster (VMC) Operator
Virtual Machine Cluster Helm Operator based on Operator SDK and built on KubeVirt.


Example cluster: 
```yaml
apiVersion: apps.baloise.dev/v1alpha1
kind: VirtualMachineCluster
metadata:
  name: example
spec:
  flavor: small
  instances: 2
  os: linux
  diskSize: 20Gi
```
