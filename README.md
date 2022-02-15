- Install [Docker](https://docs.docker.com/engine/install/) and [Compose](https://docs.docker.com/compose/cli-command/)
- Clone this repositroy `git clone git@github.com:eabykov/keycloak-compose.git`
- Change directory to `keycloak-compose`
- Up the project using command `docker compose -f docker-compose.yml -f docker-compose.monitoring.yml up -d --wait`

## After the launch

| Parameter | Value 
|-|-
| Keycloak | [http://localhost:8080](http://localhost:8080)
| Grafana | [http://localhost:3000](http://localhost:3000)
| username | `admin`
| password | `admin`

## Commands

| Command | Discription
|-|-
| `docker stats --no-stream` | Containers resource usage
| `docker compose logs` | Shows logs of containers (use flag `-f` to follow logs)
| `docker compose down` | Stop and remove containers
| `docker system prune -a -f` | Remove unused data
