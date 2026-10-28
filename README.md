# serverbaby

Docker Compose stacks for serverbaby. Each directory is one stack with its own `docker-compose.yml`.
Stacks share an external Docker network named `serverbaby`. Create it once with `docker network create serverbaby`.

Secrets live in untracked `.env` files; copy each `.env.example` to `.env` and fill it in.

| Stack | Apps | Purpose |
| --- | --- | --- |
| [arrs](arrs/) | Prowlarr, Radarr, Sonarr, cross-seed | Indexer management, movie and TV automation, cross-seeding |
| [flood](flood/) | Flood config | Config directory for the Flood UI, which runs in the qbittorrent stack |
| [homepage](homepage/) | Homepage (admin and public instances), Glances | Dashboards and host stats |
| [plex](plex/) | Plex | Media server |
| [portainer](portainer/) | Portainer CE | Docker management UI |
| [qbittorrent](qbittorrent/) | qBittorrent, Flood | Torrent client and its alternate web UI |
| [romm](romm/) | RomM, MariaDB | ROM library manager |

See [POSSIBLE_IMPROVEMENTS.md](POSSIBLE_IMPROVEMENTS.md) for security and maintenance notes.
