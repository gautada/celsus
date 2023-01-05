# Architecture Reference: Container Entrypoint

## Abstract

Applications packed within containers usually provide an entrypoint to launch the application. This process needs to support various shared services
such as logging and monitoring. This reference provides specific guidance for implementing a compatible entrypoint script for a compatable container.

## References

- https://opencontainers.org
- https://docs.docker.com/engine/reference/builder/#entrypoint
- https://developers.redhat.com/blog/2021/01/11/getting-started-with-buildah
- https://buildah.io


## Requirements

- Blocking and Background Daemon Mechanics
- Simplified/Streamlined definition - use inherited/overloading functions
- Unified Logging
- Monitoring Support


## Context Diagram



