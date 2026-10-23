# A Dummy's Guide to the Philippine Snakes 🐍

A WordPress website that helps readers identify snakes found in the Philippines — from harmless blind snakes to pit vipers.

**Live site:** [identifysnakesinph.freedev.app](https://identifysnakesinph.freedev.app) — hosted on [InfinityFree](https://www.infinityfree.com/).

![Homepage screenshot](Screenshot_5.png)

## About the project

The site presents Philippine snake species in an approachable, beginner-friendly way, with pages for:

- **Home** — introduction and getting started
- **About Me** — who is behind the guide
- **Snakes** — the species guide

It was built with **WordPress** using the **Astra** theme and the **Elementor** page builder.

## Repository contents

| File | Description |
| --- | --- |
| `compose.yaml` | Docker Compose setup for the local development environment |
| `Screenshot_5.png` | Homepage screenshot |
| `README.md` | This file |

## Local development

The site is developed locally with Docker (WordPress + MySQL 8.0).

**Requirements:** [Docker Desktop](https://www.docker.com/products/docker-desktop/)

```bash
docker compose up -d
```

Then open <http://localhost:8080> and follow the WordPress setup wizard.

The stack includes:

- **wordpress** — WordPress (latest), exposed on port `8080`
- **db** — MySQL 8.0, database `wordpress`, user `wordpress`

> These credentials are for local development only.

Data is persisted in the `wordpress_data` and `db_data` named volumes, so content survives container restarts:

```bash
docker compose down   # stops the stack, keeps volumes
docker compose down -v  # stops and removes all data
```

## Author

Built by [Franz Lyster L. Tagalogon](https://github.com/8kshj1jh44).

Cheers to more websites! <3
