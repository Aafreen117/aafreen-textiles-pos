# Base44 Dev Environment

## Project Overview
This is a single static `index.html` file — no framework, no backend, no build step, no dependencies.

## Running the App
```
docker compose -f docker-compose.base44.yml up -d
```
Serves `index.html` via nginx:alpine on host port 3000.

## Key Details
- The repo directory has restrictive (700) permissions, so the nginx worker must run as `root` (configured in `nginx.base44.conf`).
- No secrets, no environment variables, no database required.
- Edits to `index.html` are reflected immediately (file is bind-mounted, not baked into image).
- No live-reload dev server; call `reload_preview` after edits if the browser doesn't refresh.
