# Dinaip Container

## Dinaip Alpine-based image with password secured using Docker Secret

### Deploy with Compose (Secret file-based)

- Place your password in `.secrets/dinaip_passwd`.
- Ensure to secure the file with `chmod 600 .secrets/dinaip_passwd`.
- Deploy with `docker-compose up -d`

### Deploy with Compose + Swarm (Secret stored in Docker Swarm DB)

- Create your secret with:

  ```bash
  echo "your_password" | docker secret create dinaip_passwd -
  ```

* Deploy with: `docker stack deploy -c docker-compose.yml dinaip`.

* You must be in a Docker Swarm environment.

### Envarioment Variables:

* `USERNAME` (Your Account)
* `ZONES` (domain:zone1,zone2....)
