# Debugging Microservices: How Google SREs Resolve Outages

## Speakers

Adam Mckaig
Liz Fong-Jones

### Notes

- Prioritize speed and mitigation options
-  How can we improve resiliency - by formulating and testing hypotheses faster
- Google's error notitfications for SREs have playbook and silence urls in them


### Techniques

#### Layer Peeling

- Used to establish the blast radius of the outage
- They have a tool calle dpanopticon that lets the easily filter performance data for the outage
- Data is already aggregated for investigating - precomputation reduces the discovery time
- Repeatedly bisect the problem to find the root cause

#### Dynamic Data Joins

- Tricky problems can't be diagnosed with metric data
- Need to be able to use tools to write custom queries to aggregate metrics

#### Exemplars

- Make tracing useful
- Data gets tagged so we can easily move between data sets

### Wrap up

- More data that is easier to search through makes troubleshooting easier
- Add critical queries into playbooks
- Evaluate compute, storage and cognitive costs of adding precompute dashboards - too much data can be too difficulty to understand, try not to have too many dashboards
- No two outages are identical