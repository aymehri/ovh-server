# ovh-server
yum check-update
curl -fsSL https://get.docker.com/ | sh
systemctl start docker
docker run -d -p 80:80 kitematic/hello-world-nginx
