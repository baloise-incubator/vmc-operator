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
    os: linux
    platform: openshift
    instances: 1
    nameOverride:
    diskSize: 20Gi
    ports:
      - name: https
        port: 443
        backendPort: 8443 # optional - defaults to port
        protocol: TCP # optional - defaults to TCP
```