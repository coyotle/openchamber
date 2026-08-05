# OpenChamber

Self-hosted Docker image of [OpenChamber](https://github.com/openchamber/openchamber) — an open-source workspace for running, supervising, and reviewing AI coding work across desktop, browser, editor, and mobile.

## What is this repo?

This repository contains a GitHub Actions workflow that automatically builds and publishes a Docker image from the upstream [openchamber/openchamber](https://github.com/openchamber/openchamber) releases to GitHub Container Registry.

## Pull

```bash
docker pull ghcr.io/coyotle/openchamber:latest
```

## How it works

A daily cron job checks the latest release of the upstream repo. If a new version is detected, the workflow clones the source, builds a multi-arch Docker image (`linux/amd64`, `linux/arm64`), and pushes it to GHCR with the release tag.
