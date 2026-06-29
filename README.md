# Docker Compose Homelab

A self-hosted infrastructure setup using Docker Compose, managing multiple
services for personal and development use.

## 🔧 Services

| Service             | Purpose                                     |
| ------------------- | ------------------------------------------- |
| **actual**          | Personal finance tracking and budgeting     |
| **alloy**           | Collects metrics data                       |
| **blocky**          | DNS-level ad blocking                       |
| **forgejo**         | Lightweight self-hosted Git service         |
| **forgejo-runner**  | CI/CD runner for Forgejo actions            |
| **Garage**          | S3 API server for backups with Restic       |
| **grafana**         | Visualization, dashboards, and monitoring   |
| **immich**          | Photo and video backup solution             |
| **llama-server**    | Local LLM inference server                  |
| **minecraft**       | Minecraft game server                       |
| **node-exporter**   | System-level hardware and OS metrics        |
| **stalwart**        | Complete mail server solution               |
| **traefik**         | Modern HTTP reverse proxy and load balancer |
| **transmission**    | Lightweight BitTorrent client               |
| **vaultwarden**     | Password manager (Bitwarden compatible)     |
| **victorialogs**    | Time series log management                  |
| **victoriametrics** | Fast, cost-effective monitoring stack       |

## Configuration Management

### Node Configuration

Node-level configurations are stored in the `_node-configs` directory.

### Service Configuration

Each service maintains its own configuration in the `_configs/` directory:

```bash
apps/<service>/
├── docker-compose.yml    # Service definition
└── _configs/             # Service-specific configuration files
    └── *.yml             # Configuration files (mounted as volumes)
```

### Environment Variables

The `.env` file contains sensitive configuration. Never commit this file to
version control. It's included in `.gitignore` by default.
