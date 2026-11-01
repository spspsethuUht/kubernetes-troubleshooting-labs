FailedScheduling
Objective
Demonstrate scheduler failure when requested resources exceed cluster capacity.

YAML Used
scheduling-demo.yaml

Commands Executed
kubectl apply -f scheduling-demo.yaml
kubectl get pods
kubectl describe pod scheduling-demo
Expected Result
Pending
FailedScheduling
Root Cause
Requested CPU or memory exceeds available node resources.

Troubleshooting Steps
kubectl describe pod scheduling-demo
Review scheduler events.

Resolution
Reduce resource requests or add cluster capacity.