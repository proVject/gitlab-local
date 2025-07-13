# Gitlab-local

1. Install docker and docker CE - https://docs.docker.com/engine/install/ubuntu/
2. on your server
```bash
mkdir ~/gitlab && cd cd ~/gitlab && git clone https://github.com/proVject/gitlab-local.git .
```
3. replace the in docker-compose.yml
   - hostname to your domain or ip
   - environment GITLAB_OMNIBUS_CONFIG

4. add DNS record on your domain 
A gitlab <YOUR_IP> dns only 10
5. run the container 
```bash
docker compose up -d 
```
it can take some time to initialize the container

6. get your root password
```bash
root@cliwave:~/gitlab# docker exec -it gitlab cat /etc/gitlab/initial_root_password
#Password: <YOUR ROOT PASSWORD>
```

7. open [gitlba.<YOUR_DOMAIN>](https://gitlab.example.com)



