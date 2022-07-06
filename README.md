# Relay (TOR)

This repository contains source code for the simple Protokolla Relay info page.

## Setup

1. Install tor relay
2. Configure tor relay
3. Setup following DNS records:
```
A tor-relay-1.palvelin IN this.ip.add.ress
CNAME relay IN tor-relay-1.palvelin
```
4. Clone this repository to /var/www/html
5. Install apache2 (`apt install apache2`)
6. Install certbot (`apt install certbot`)
7. Add certbot to crontab (`0 12 * * * /usr/bin/certbot renew --quiet`)

## Future

1. Make ansible script for automatic setup
2. Link todo.protokolla.fi kanbana here