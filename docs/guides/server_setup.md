# Initial Server Setup

## 1. Create Sudo User

```bash
adduser filippo
usermod -aG sudo filippo
rsync --archive --chown=filippo:filippo ~/.ssh /home/filippo
```

## 2. Install docker and docker-compose

```bash
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
apt-cache policy docker-ce
sudo apt install docker-ce
sudo systemctl status docker
sudo usermod -aG docker filippo

sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

## 3. Install Nginx

```bash
sudo apt update
sudo apt install nginx
systemctl status nginx
```

## 4. Install Certbot

```bash
sudo apt install certbot python3-certbot-nginx
```

## 5. Install and Configure cron

```bash
sudo apt update
sudo apt install cron
sudo systemctl enable cron

crontab -e
# * * * * * /usr/local/bin/docker-compose -v >> /home/deployer/cron/out.log 2>&1

crontab -l
```

## 6. Firewall setup. Allow only Nginx

```bash
sudo ufw enable
sudo ufw allow ssh
sudo ufw status
sudo ufw app list
sudo ufw allow 'Nginx HTTPS'
```