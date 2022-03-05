## Wait for the https://github.com/keycloak/keycloak/issues/10216 to be fixed

1. Install [Docker](https://docs.docker.com/engine/install/) and [Compose](https://docs.docker.com/compose/cli-command/)
2. Up the project using command `docker compose up -d --wait`
3. Import realm by command `docker compose exec keycloak /bin/sh -c '/opt/keycloak/bin/kc.sh import --file /tmp/realm.json'`
4. Restart keycloak `docker compose restart keycloak`

## After the launch

| App | Url | Username | Password 
|-|-|-|-
| Keycloak | [http://localhost:8080](http://localhost:8080) | `admin` | `keycloak`
| Grafana | [http://localhost:3000](http://localhost:3000) | `admin` | `grafana`

![Grafana Keycloak Dashboard](./images/image.png)

## Commands

| Command | Discription
|-|-
| `docker stats --no-stream` | Containers resource usage
| `docker compose logs` | Shows logs of containers (use flag `-f` to follow logs)
| `docker compose down` | Stop and remove containers (flag `-v` remove named volumes declared in the volumes section of the Compose file and anonymous volumes attached to containers)
| `docker system prune -a -f` | Remove all unused containers, networks, images (flag `--volumes` prune volumes)
