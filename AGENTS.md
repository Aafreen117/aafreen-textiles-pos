# Base44 dev environment

This repo is a static single-page site: only `index.html` exists (no framework, backend, or dependencies).

## Run
`docker compose -f docker-compose.base44.yml up -d` — serves `index.html` via nginx:alpine on host port 3000.

## Verify
`curl -s -o /dev/null -w "%{http_code}" http://localhost:3000/` should return 200.

## Notes
- No build step, no migrations, no secrets required.
- To edit content, change `index.html` and reload the preview.
