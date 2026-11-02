Service Selector Mismatch
Objective
Demonstrate a service routing issue caused by label mismatch.

YAML Used
pod.yaml service.yaml

Commands Executed
kubectl apply -f pod.yaml
kubectl apply -f service.yaml

kubectl get svc
kubectl get endpoints
Expected Result
No Endpoints
Root Cause
Service selector labels do not match pod labels.

Troubleshooting Steps
kubectl get endpoints
kubectl describe svc nginx-service
Verify labels and selectors.

Resolution
Update Service selector to match Pod labels.