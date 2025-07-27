. 🚀 Launch Node Exporter on EC2
SSH into the EC2 server and run:

Necessary Packages Installation on AWS EC2
Install these Packages

# Updates the package index to ensure you have the latest information about #available packages.
sudo apt-get update -y = ubuntu
    yum for ec2

# Installs Docker from the default Ubuntu package repository.
sudo apt install docker.io -y
sudo yum install docker -y = ec2

# Adds the 'ubuntu' user to the 'docker' group, allowing the user to run Docker #commands without sudo.
for bith ec2 or ubuntu
sudo usermod -aG docker $USER

NOTE: # Then log out and log back in (or run newgrp docker) for the changes to take effect #

sudo chmod 777 /var/run/docker.sock

sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose


# Makes the Docker Compose binary executable.
sudo chmod +x /usr/local/bin/docker-compose

# Verifies the installation of Docker Compose by displaying its version.
docker-compose --version 

2. 📦 Deploy Monitoring Stack
git clone https://*******************
cd ec2-monitoring-with-grafana-prometheus
sudo docker-compose -f "./build-process/docker-compose.yml" up -d --build

4. 📊 Access Grafana
URL: http://YOUR_SERVER_IP:3000
Default login: admin / admin
Import Dashboard ID: 1860 (Node Exporter Full)

