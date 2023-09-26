# CI-CD-pipelines

Jenkins CI/CD pipelines

## Running on Windows

```shell
    docker run --name jenkins-blueocean --restart=on-failure --detach \
    --network jenkins --env DOCKER_HOST=tcp://docker:2376 \
    --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 \
    --volume jenkins-data:/var/jenkins_home \
    --volume jenkins-docker-certs:/certs/client:ro \
    --publish 8080:8080 --publish 50000:50000 myjenkins-blueocean:2.414.2-1
```

## Get the Password

```bash
    docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword
```
