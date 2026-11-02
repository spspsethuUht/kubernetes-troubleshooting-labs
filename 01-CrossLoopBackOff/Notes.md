CrashLoopBackOff
Objective
Demonstrate how Kubernetes reacts when a container continuously exits after startup.

YAML Used
crashloopbackoff.yaml

Commands Executed
kubectl apply -f crashloopbackoff.yaml
kubectl get pods
kubectl logs crashloop-demo
kubectl describe pod crashloop-demo
Expected Result
CrashLoopBackOff
Root Cause
Container exits immediately with a non-zero exit code.

Troubleshooting Steps
kubectl logs crashloop-demo
kubectl describe pod crashloop-demo
Review container logs and restart count.

Resolution
Fix application startup logic.