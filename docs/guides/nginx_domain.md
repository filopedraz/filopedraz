# New Domain with Nginx and Let's Encrypt

## 1. Create the domain configuration file and link it accordingly

```bash
sudo vim /etc/nginx/sites-available/{DOMAIN}
sudo ln -s /etc/nginx/sites-available/{DOMAIN} /etc/nginx/sites-enabled/

sudo nginx -t
sudo systemctl restart nginx
```

## 2. Run certbot on that specific domain

```bash
sudo certbot --nginx -d {DOMAIN}

sudo systemctl status certbot.timer
sudo certbot renew --dry-run
```