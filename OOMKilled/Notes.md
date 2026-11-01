OOMKilled (Exit Code 137)
Objective
Demonstrate how Kubernetes terminates a container when it exceeds its configured memory limit.

YAML Used
oomkilled.yaml

Commands Executed
kubectl apply -f oomkilled.yaml
kubectl get pods
kubectl describe pod oom-demo
Expected Result
OOMKilled
Exit Code 137
Root Cause
Application consumes memory beyond the configured container limit.

Troubleshooting Steps
kubectl describe pod oom-demo
Review Last State section.

Resolution
Increase memory limits or optimize application memory usage.