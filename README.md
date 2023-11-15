# ha-template

This is Helm Chart for a deployment running in High Availability mode.

This Helm chart includes the following templates:

- Namespace
- Deployment
- Service
- Route

The deployment manifest implements the following options:

- 3 Replicas.
- Readiness Probe.
- Liveness Probe.
- `seccomp` Profile.
- Security Context capabilities.
- Resources Requests.
- Resources Limits.
- Pod Anti-Affinity.
- Run the pod in non-privileged mode.
- Prevent the container from privilege escalation
- Run container with a non-root user.

> Note: The resources requests and limits uses if-else logic to ensure that there's default value if the deployer does not enter a value.

**This repo is meant to be a reference point for creating helm chart with the above options, it will need to be amended to accommodate varying requirements for application deployments.**
