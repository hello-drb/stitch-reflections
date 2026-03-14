# Stitch Reflections

Handcrafted crochet showcase website for Stitch Reflections by Selena.

## Setup

This is a static HTML site. To serve it locally:

```bash
python3 -m http.server 8080
```

Or on your droplet, clone and serve via nginx:

```bash
git clone https://github.com/hello-drb/stitch-reflections.git /var/www/stitch-reflections
```

### Nginx config example

```nginx
server {
    listen 80;
    server_name your-droplet-ip;
    root /var/www/stitch-reflections;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

## Images

Add product photos to the `images/` directory. The HTML references them from `images/` paths.

## Structure

```
├── index.html          # Main site
├── images/             # Product photography
│   ├── IMG_7475.jpg
│   ├── IMG_7481.jpg
│   └── ...
└── README.md
```
