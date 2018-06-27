# Clever: Control Planes: Designing Infrastructure for Rapid Iteration

## Speaker

Mohit Gupta

### Notes

- If you move fast, you can find the time to think later (pretend that it works for a little while)
- Leap of faith - if big companies use it, we can too
- Service discovery - get dependencies from discovery
- Smple syntax to start an app on an environment, - Starts dependencies in that env if they don't exist
- Engineers are users too

## Core Principles Around Building Control Planes

- Control Plane is a simple API/surface that people know how to use (e.g. with deployment here)
- Allow for rapid infrastructure experimentation
- First a UI then an API, then you can iterate on the infrastructure
- Start with thin wrappers
- Find your own defaults
- Highlight your quirks
- Outsource complexity when possible
- The set themselves up for success to switch backing technologies by building a layer on top - and an api that provided clarity on what was happening on infrastructure
- Implemented on top of ECS (their tool is called ARK): canary deploys, dameon containers, cross-cluster environments, autoscaling
- They can autoscale easily because they know when demand is coming (K-12 products)
- Asynchronous Workflows: like airflow - but with the speed of docker containers - more than 1M executions per week, over 100 asynchronous workers (https://github.com/Clever/workflow-manager) - docker container shim that allows containers to be used by AWS step functions. Built resume on top of it. Replaced their use of AWS batch