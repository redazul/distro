```
sudo apt update
sudo apt install nginx
sudo apt install certbot python3-certbot-nginx
sudo certbot --nginx -d mint.blendhit.com
sudo chown ubuntu:ubuntu /var/www/html -R
echo '{"domain": "mint.blendhit.com", "certificate_path": "/etc/letsencrypt/live/mint.blendhit.com/fullchain.pem", "private_key_path": "/etc/letsencrypt/live/mint.blendhit.com/privkey.pem"}' > cert.json
sudo nginx -t
sudo systemctl reload nginx
