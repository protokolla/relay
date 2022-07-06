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
4. Install apache2 (`apt install apache2`)
5. Install git (`apt install git`)
6. Clear `/var/www/html` directory (`rm /var/www/html/*`)
7. Clone this repository to `/var/www/html` (`git clone https://github.com/protokolla/relay.git .`)
8. Install certbot (`apt install certbot`)
9. Install apache plugin for certbot (`apt install python-certbot-apache`)
10. **DOES NOT WORK** Setup cert (`certbot --apache --noninteractive --domain relay.protokolla.fi --agree-tos --email relay@protokolla.fi`)
11. Add certbot to crontab (`0 12 * * * /usr/bin/certbot renew --quiet`)

## Future

1. Make ansible script for automatic setup
2. Enable htaccess https://askubuntu.com/questions/429869/is-this-a-correct-way-to-enable-htaccess-in-apache-2-4-7
3. Fix certbot
4. Link todo.protokolla.fi kanbana here