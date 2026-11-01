CreateContainerConfigError - Missing ConfigMap
Objective
Demonstrate container startup failure when a required ConfigMap is missing.

YAML Used
config-error-demo.yaml

Commands Executed
kubectl apply -f config-error-demo.yaml
kubectl get pods
kubectl describe pod config-error-demo
Expected Result
CreateContainerConfigError
Root Cause
Referenced ConfigMap does not exist.

Troubleshooting Steps
kubectl describe pod config-error-demo
Check Events section.

Resolution
Create the required ConfigMap before deploying the pod.