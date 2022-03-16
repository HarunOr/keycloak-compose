1. Install [Docker](https://docs.docker.com/engine/install/) and use [v2.3.3](https://github.com/docker/compose/releases/tag/v2.3.3) of the [Compose](https://docs.docker.com/compose/cli-command/)
2. Up the project using command `docker compose up -d --wait`

## Links and images

| App | Port | Username | Password 
|-|-|-|-
| Keycloak | 8080 | `admin` | `keycloak`

![Keycloak Grafana Client in the realm test](./images/keycloak.jpg)

| App | Port 
|-|-
| Prometheus | 8090

![Prometheus Targets](./images/prometheus.jpg)

| App | Port | Username | Password 
|-|-|-|-
| Grafana | 3000 | `admin` | `grafana`

![Grafana Keycloak Dashboard](./images/grafana.png)

## Usefull commands

| Command | Discription
|-|-
| `docker stats --no-stream` | Containers resource usage
| `docker compose logs` | Shows logs of containers (use flag `-f` to follow logs)
| `docker compose down` | Stop and remove containers (flag `-v` remove named volumes declared in the volumes section of the Compose file and anonymous volumes attached to containers)
| `docker system prune -a -f` | Remove all unused containers, networks, images (flag `--volumes` prune volumes)
