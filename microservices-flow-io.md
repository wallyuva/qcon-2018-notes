# Design Microservice Architectures the Right Way

## Speakers 

Michael Bryzek (formerly Gilt CTO)


### Notes

- Super expensive to adopt new frameworks and programming languages
- Code generation can be valuable - having a agreed upon schema, using conventions for methods, user friendly urls
- Events are critical parts of an interface but its ok for services to be the system of record for their resources
- Investing in autoation and toolimg allows developers to own more microservices
- Creating a databse is just as easy as creating an api, can describe db needs in a manifest, enforce no empty strings for data exports, hashcode to only run db operations when records change, normalize access to db, create indexes by default when necessary

## API definitions

- Schema indicatates through annotations which fields have personal data (GDPR)
- Api defnitions are in a git repo, run CI on that repo (linting, etc), verify potentially breaking changes
- API builder (open source tool from Gilt)
- API impplementation supported by cide generation: generate routes file, client and mock client (enables high fidelity, fast testing)
- Automatically update all services to latest dependencies (dependency.flow.io - open source project)

### CD

- Deploy triggered by a git tags
- Git tags created automatically by a change on master
- 100% automated, 100% reliable
- Dashboard to see what is deployed
- Configuration - keep it simple
- Once it's green, deploy it!

### Events

- Prefer consumers (including interanl) to use events instead of apis
- First class schema for all events
- Consumers implement idempotency
- Producers - journal of all operations on table, publissh 1 event per journal record, enable replay by simply requeuing journal record
- Consumers - sotre events locally, partitioned for fast removal, process micro batches and record failures locally (publish them to a monitoring system)
- Event schemas - 1 model/event, 1 union type/ stream, stream owned by 1 service, lint event schemas
- Journaling defined by schema as well, tells how long to keep journal partitions
- Stream names are determined useing reflection
