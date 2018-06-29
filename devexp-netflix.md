# Better DevEx at Netflix: Polyglot and Containers

## Speakers

J. Michael McGarr

### Notes

- Build tool -> Develeper Workflow Tool (NEWT)
  - Language agnostic
  - Reduce cognitive load for engineers
  - Chose go so you could write easily distributable binaries (and command line tools)
  - Node.js developers don't have to install java (for gradle, etc)
  - Tool checks for dependencies on local machines - self-configures and installs dependencies
  - Can provide config files fot the tool (to tell newt what build script to run, etc.)
  - Manages dependencies
- Gains
  - Simplified packaging
  - Tooling consistency
  - Tool environment islation
  - Agnostic to build tools
- App type templates - use newt to generate apps
  - Creates git repo
  - Creates jenkins builds
  - Creates spinnaker pipeline
  - Within 1-1.5 minutes all infrustructe is in place so you can just focus on coding
- Added a command to report errors
- Newt takeaways
  - It's not a tool, its a platform!
  - Containers and good build tools/platforms make polyglot less expensive
  - Build platforms, not tools and proide native solutions
  - Reduce cognitive load