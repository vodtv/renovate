# renovate
Shared Renovate presets for VODTV projects.

## Presets
- default: node-app
- node-app: Node.js application
- node-lib: Node.js library / SDK
- docker: Docker image project
- monorepo: PNPM monorepo

## Usage
### Default (node-app)
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>vodtv/renovate"]
}
