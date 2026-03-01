Docker Setup Commands

1. Pull Latest Changes from Repository

```
git pull
```

Description:
Fetches and merges the latest changes from the remote Git repository into your current branch.
Use this before starting Docker containers to ensure you are running the latest code.

---

2. Start API Gateway Service

```
sudo docker compose -f docker-compose.api-gateway.yml up -d
```

Description:
Starts the API Gateway service in detached mode using the `docker-compose.api-gateway.yml` configuration file.

* `-f` → Specifies the compose file
* `up` → Creates and starts containers
* `-d` → Runs containers in the background
* `sudo` → Required if Docker needs elevated privileges

---

3. Start Server Service

```
docker compose -f docker-compose.server.yml up -d
```

Description:
Starts the server service in detached mode using the `docker-compose.server.yml` file.

---

4. Rebuild and Start Server Service

```
docker compose -f docker-compose.server.yml up -d --build
```

Description:
Rebuilds the Docker images and then starts the server service in detached mode.

Use this when:

* You have made code changes
* Dependencies were updated
* Dockerfile was modified

