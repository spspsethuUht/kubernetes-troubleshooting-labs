CreateContainerConfigError - Missing Secret
Objective
Demonstrate container startup failure when a required Secret is missing.

YAML Used
secret-error-demo.yaml

Commands Executed
kubectl apply -f secret-error-demo.yaml
kubectl get pods
kubectl describe pod secret-error-demo
Expected Result
CreateContainerConfigError
Root Cause
Referenced Secret does not exist.

Troubleshooting Steps
kubectl describe pod secret-error-demo
Review Events section for Secret-related errors.

Resolution
Create the required Secret before deploying the pod.