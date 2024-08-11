# FiveM server boilerplate

A FiveM server under Docker with minimal resources as Git submodules.

## Requirements

- Docker
- Git
- Node.js
- pnpm

## How to use it?

To manage certain resources, you need to install them via Git submodules.

- `git submodule update --init`

Now, you need to build the dependencies that require it (here, oxmysql).

1. `pnpm --dir resources/oxmysql/ i --frozen-lockfile`
2. `pnpm --dir resources/oxmysql/ run build`

All that's left is to start the server.

- `docker compose up -d`
