Liveness Probe Failure
Objective
Demonstrate automatic container restarts caused by failing liveness checks.

YAML Used
liveness-fail-demo.yaml

Commands Executed
kubectl apply -f liveness-fail-demo.yaml
kubectl get pods
kubectl describe pod liveness-fail-demo
Expected Result
Restart Count increases continuously.
Root Cause
Liveness probe points to an invalid endpoint.

Troubleshooting Steps
kubectl describe pod liveness-fail-demo
Check Events section for probe failures.

Resolution
Correct liveness probe configuration.