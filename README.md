# Homelab server environment

## Setup

```bash
podman compose -f homeassistant/podman-compose.yaml up -d
```

The `-d` flag ensures that the containers are running in the background,
and not outputing to your shell.

## Shutdown

```bash
podman compose -f homeassistant/podman-compose.yaml down -v
```

The `-v` flag ensures that the container is properly removed.

## Purging

First run the shutdown commands,
then remove all subdirectories of the projects such that
the containers must create new volumes.
