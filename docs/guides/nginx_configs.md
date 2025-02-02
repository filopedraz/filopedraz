# Nginx Configurations

## Django

```nginx
server {
    server_name {SERVER_NAME};

    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-Host $host:$server_port;
        proxy_set_header X-Forwarded-Server $host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

## React

```nginx
server {
    server_name {SERVER_NAME};

    location / {
        proxy_pass http://localhost:3000;
        try_files $uri $uri/ /index.html =404;
    }
}
```