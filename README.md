Kubernetes Troubleshooting Labs
Overview
This repository contains hands-on Kubernetes troubleshooting scenarios executed on Minikube.

The purpose of this project is to practice identifying, analyzing, and resolving common Kubernetes failures using:

kubectl get pods
kubectl describe pod
kubectl logs
kubectl get events
Service troubleshooting
Resource troubleshooting
Probe troubleshooting
All scenarios were reproduced in a local Minikube cluster.

Environment
Kubernetes
Minikube
kubectl
Docker
Troubleshooting Scenarios
#	Scenario	Status
1	ImagePullBackOff	?
2	CrashLoopBackOff	?
3	OOMKilled (Exit Code 137)	?
4	Missing ConfigMap	?
5	Missing Secret	?
6	FailedScheduling	?
7	FailedMount	?
8	Readiness Probe Failure	?
9	Liveness Probe Failure	?
10	Service Selector Mismatch	?
Lab Structure
Each lab contains:

YAML definition
Commands executed
Screenshot evidence
Root cause analysis
Resolution steps
Scenario 1 – ImagePullBackOff
Symptoms
Pod does not start.

Commands
kubectl describe pod imagepull-demo

Root Cause
Invalid image name or unavailable image registry.

Resolution
Use a valid image and redeploy.

Scenario 2 – CrashLoopBackOff
Symptoms
Container repeatedly restarts.

Commands
kubectl logs crashloop-demo

kubectl describe pod crashloop-demo

Root Cause
Application exits with a non-zero status code.

Resolution
Fix application startup logic.

Scenario 3 – OOMKilled (Exit Code 137)
Symptoms
Container restarts due to memory exhaustion.

Commands
kubectl describe pod oom-demo

Root Cause
Container exceeded memory limit.

Resolution
Increase memory limit or optimize memory usage.

Scenario 4 – Missing ConfigMap
Symptoms
CreateContainerConfigError

Root Cause
Referenced ConfigMap does not exist.

Scenario 5 – Missing Secret
Symptoms
CreateContainerConfigError

Root Cause
Referenced Secret does not exist.

Scenario 6 – FailedScheduling
Symptoms
Pod remains Pending.

Root Cause
Insufficient cluster resources.

Scenario 7 – FailedMount
Symptoms
Volume mount failure.

Root Cause
Secret or volume unavailable.

Scenario 8 – Readiness Probe Failure
Symptoms
Pod Running but not Ready.

Root Cause
Incorrect readiness endpoint.

Scenario 9 – Liveness Probe Failure
Symptoms
Container continuously restarts.

Root Cause
Incorrect liveness endpoint.

Scenario 10 – Service Selector Mismatch
Symptoms
Service has no endpoints.

Commands
kubectl get endpoints

Root Cause
Selector labels do not match Pod labels.

Key Kubernetes Commands Used
kubectl get pods

kubectl describe pod

kubectl logs

kubectl get events

kubectl get endpoints

kubectl top pod

kubectl exec -it

Skills Demonstrated
Kubernetes Administration
Troubleshooting
Container Diagnostics
Resource Management
Networking
Storage Troubleshooting
Service Discovery
Health Checks
Root Cause Analysis
Author
Sethu

26+ years IT experience

Learning Kubernetes, SRE, DevOps, Observability and Cloud Technologies.