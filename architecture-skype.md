# Skype's Journey From P2P: It's Not Just About the Services

## Speakers

Bruce Lowekamp

### Notes

- P2P architecture makes it difficult to upgrade clients and turns mobile phones into pocket heaters
- Gradual changes to the architecture to move to service based
- Recorded netrics for those changes - objective metrics could be skewed due to who was downloading the new clients, need A/B testing instead

#### When to use A/B testing

- For data-drien decisions
- Only valid method to draw inference about what the code changes actually impacted since the user set is not skewed

### Experimentation Practices

- Label expirements by type, expermient id, iteration
- Back end evaluates the hash of the expirement ot figure out eactly which client is being tested
- Sometimes you know expirements can be risky so you need to cap their time
- Scorecards are necessary to determine unintended consequences of expirments

## Lessons learned
- Make apps configurable for migrations and picj the appropriate strategy for migration based on complexity
- Don't bake in experiments, what not why!