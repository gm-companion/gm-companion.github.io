---
title: "Backend"
description: "All about the self-hostable backend service."
weight: 10
---

Some workflows are easier with a separate backend service.
At the moment this is only the case for connecting to Spotify.

An instance of the backend is hosted at https://gm-companion.rophil.lol, but you can also host it yourself.
If that is the case, follow the steps below.

## Source Code

The source code is hosted at [GitHub](https://github.com/gm-companion/gm-companion-backend) and the docker image is built using GitHub Actions and published via the GitHub Container Repository.

## Installation

The backend is available as a docker image at `ghcr.io/gm-companion/backend`.

### Config

Configuration is done through environment variables:

#### Required

`SPOTIFY_CLIENT_ID` and `SPOTIFY_CLIENT_SECRET` are required.  
These can be acquired by registering an application at https://developer.spotify.com.
The redirect URI is `http://localhost:59992`.

#### Optional

`SENTRY_DSN` is only useful for automatic error reporting via [sentry.io](https://sentry.io/). Your instance probably does not need it.

### Docker Compose

You can use the following docker compose file:

```yaml
version: "3"
services:
  backend:
    image: ghcr.io/gm-companion/backend:latest
    container_name: gm-companion-backend-dev
    restart: unless-stopped
    ports:
      - "40001:3000"
    environment:
      - TZ=Europe/Berlin
      - NODE_ENV=production
      - SPOTIFY_CLIENT_ID=
      - SPOTIFY_CLIENT_SECRET=
```
