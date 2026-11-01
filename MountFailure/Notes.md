FailedMount
Objective
Demonstrate pod startup failure due to unavailable volume resources.

YAML Used
mount-failure-demo.yaml

Commands Executed
kubectl apply -f mount-failure-demo.yaml
kubectl get pods
kubectl describe pod mount-failure-demo
Expected Result
FailedMount
Root Cause
Referenced Secret or volume does not exist.

Troubleshooting Steps
kubectl describe pod mount-failure-demo
Check Events section.

Resolution
Create the required Secret or volume resource.