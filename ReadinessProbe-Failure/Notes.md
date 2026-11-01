Readiness Probe Failure
Objective
Demonstrate how a pod can remain running but unavailable for service traffic.

YAML Used
readiness-fail-demo.yaml

Commands Executed
kubectl apply -f readiness-fail-demo.yaml
kubectl get pods
kubectl describe pod readiness-fail-demo
Expected Result
READY 0/1
Running
Root Cause
Readiness probe points to an invalid endpoint.

Troubleshooting Steps
kubectl describe pod readiness-fail-demo
Review readiness probe failures.

Resolution
Update probe path, port, or application endpoint.