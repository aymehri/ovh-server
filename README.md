# ovh-server
see https://gist.github.com/wdullaer/f1af16bd7e970389bad3

```sh
yum check-update
yum -y install vim git zip bzip2 fontconfig curl

# Install docker
curl -fsSL https://get.docker.com/ | sh
# Make docker lunch at startup 
systemctl start docker
# Test Docker
docker run -d -p 80:80 kitematic/hello-world-nginx

# Install docker-compose
COMPOSE_VERSION=`git ls-remote https://github.com/docker/compose | grep refs/tags | grep -oP "[0-9]+\.[0-9][0-9]+\.[0-9]+$" | tail -n 1`
sudo sh -c "curl -L https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose"
sudo chmod +x /usr/local/bin/docker-compose
sudo sh -c "curl -L https://raw.githubusercontent.com/docker/compose/${COMPOSE_VERSION}/contrib/completion/bash/docker-compose > /etc/bash_completion.d/docker-compose"

```
