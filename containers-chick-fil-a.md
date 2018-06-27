# Chick-Fil-A: Milking the Most Out of 1000's of K8s Clusters

## Speakers

- Brian Chambers - IOT/Edge Computing @brianchambers21
- Caleb Hurd - SRE @calebrhurd

## Architecture

Kubernetes
istio
Prometheus

## Notes

- K8s helps you focus on the development of microservices and not deal with the other stuff (security, etc) through a good toolset
- Book: Accelerate: The Science of Lean Software and DevOps: Forsgren

### Cloud-fil-A

- Some computing needs to happen locally because of intermittent connectivity
- Small boxes that run a bare metal version ofk k8s
- Bare metal clusters simple enough for non-technologist to install, manageable remotely, self-healing and highly available


## Tooling

- Kops, Kubespray, kubeadmin, Rancher Kubernetes Engine (fast and easy, tehir choice)
- Resetting Cluster State with Overlay FS + HAMS (can undo things when the cluster gets borked - restore to initial state)
- Hooves Up - open source tool they built- self healing AWS SSM Registration, can do remote commands and patch reporting/management

## Lessons Learned from SRE

- Use K8s feature set, dont reinvent the wheel
- MVP MVP MVP (always get the job done, even if it's not pretty)
- Ensure aggregated and searchable logging (necessary for scale)
- Deep health checks required
- Every service needs a /metrics endpoint

## Fleet - their SSDR

- Simple to use
- Declarative
- Supports multiple deployment models blue/green, canary
- Rollout over flexible time period
- Leverage standard k8s API
- Full visibility
- there is an API for deploying!!! - it templates out files, puts them in their Atlas repo so you can see what happened with deployments
- Dynamo table keeps records of the deployments (deployment hash, git hash, target, status)