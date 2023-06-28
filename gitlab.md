# gitlab-ctl
```
docker exec -it GITLAB_CONTAINER_ID /bin/bash
```
# gitlab arm64 v8
``` 
sudo docker run --detach \
  --hostname gitlab.example.com \
  --publish 443:443 --publish 80:80 --publish 20:22 \
  --name gitlab \
  --restart always \
  --volume $GITLAB_HOME/config:/etc/gitlab \
  --volume $GITLAB_HOME/logs:/var/log/gitlab \
  --volume $GITLAB_HOME/data:/var/opt/gitlab \
  --shm-size 256m \
  yrzr/gitlab-ce-arm64v8:latest
```
