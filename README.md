# Docker Compose Homelab

A self-hosted infrastructure setup using Docker Compose, managing multiple
services for personal and development use.

## 🔧 Services

| Service             | Description              | Purpose                                          |
| ------------------- | ------------------------ | ------------------------------------------------ |
| **actual**          | Actual Budget            | Personal finance tracking and budgeting          |
| **alloy**           | Time Series Database     | Collects metrics data                            |
| **blocky**          | DNS Ad-Blocker           | DNS-level ad blocking                            |
| **cadvisor**        | Container Advisor        | Container resource usage and performance metrics |
| **forgejo**         | Forgejo                  | Lightweight self-hosted Git service              |
| **forgejo-runner**  | Forgejo Runner           | CI/CD runner for Forgejo actions                 |
| **grafana**         | Grafana                  | Visualization, dashboards, and monitoring        |
| **immich**          | Immich                   | High-performance photo and video backup solution |
| **llama-server**    | llama.cpp Server         | Local LLM inference server                       |
| **minecraft**       | Minecraft Server         | Minecraft game server                            |
| **node-exporter**   | Prometheus Node Exporter | System-level hardware and OS metrics             |
| **stalwart**        | Stalwart Mail Server     | Complete mail server solution                    |
| **traefik**         | Traefik                  | Modern HTTP reverse proxy and load balancer      |
| **transmission**    | Transmission             | Lightweight BitTorrent client                    |
| **vaultwarden**     | Vaultwarden              | Password manager (Bitwarden compatible)          |
| **victorialogs**    | VictoriaLogs             | Time series log management                       |
| **victoriametrics** | VictoriaMetrics          | Fast, cost-effective monitoring stack            |

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
