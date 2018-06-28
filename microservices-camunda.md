# Complex Event Flows in Distributed Systems

## Speaker

Bernd Rücker

### Notes

- Complex event chains set you up for trouble in the future (Fowler)
- Peer to peer event chains make it defficult to change the processing order
- Issuing commands - or an intent about what needs to happen in the future - helps to avoid complexity
- Fowler: Smart endpoints and dumb pipes (Make event bus as dumb as possible)
- Newmann - A few smart god services telling anemic CRUD services what to do (is this Harmony ;) ???)
- Always think about resposbility when designing event systems so it is clear what issues can be handled by what services

## Satte Machines

- Netflix Conductor, Uber Cadence, AWS Step Functions, Zeebe by Camunda - don't DIY
- What is a lightweight workflow engine
- Synchronous communication issues can lead you to create more stateful patterns - e.g. long running retries
- Relaxed consistency - temporalrily inconsistent but eventally consistent (e.g. AirBnb takes voucher right away but does not confirm booking until later)
