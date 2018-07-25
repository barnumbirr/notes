# Using letsencrypt to generate an SSL cert

Install git:
```
sudo apt-get update
sudo apt-get install git
```

Get letsencrypt form the official Github repo:
```
git clone https://github.com/letsencrypt/letsencrypt /opt/letsencrypt
```

Add the following location to the Nginx HTTP vhost:
```
location ^~ /.well-known/acme-challenge/ {
    root /var/www/letsencrypt;
    allow all;
}
```

For Apache, use:
```
Alias /.well-known/acme-challenge/ "/var/www/letsencrypt/.well-known/acme-challenge/"
<Directory "/var/www/letsencrypt/">
    AllowOverride None
    Options MultiViews Indexes SymLinksIfOwnerMatch IncludesNoExec
    Require method GET POST OPTIONS
</Directory>
```

Request a certificate:
```
root@host:/opt/letsencrypt# ./letsencrypt-auto certonly --webroot -w /var/www/letsencrypt/ --rsa-key-size 4096 -d your_domain.tld -d your_domain2.tld -d your_domain3.tld
```

Generate a Diffie-Hellman key:
```
openssl dhparam -out /etc/letsencrypt/live/your_domain.tld/dhparam.pem 2048
```

Add the following to the Nginx HTTPS vhost:
```
    ssl on;
    ssl_certificate /etc/letsencrypt/live/your_domain.tld/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/your_domain.tld/privkey.pem;
    ssl_dhparam /etc/letsencrypt/live/your_domain.tld/dhparam.pem;
    ssl_session_timeout 5m;
    ssl_prefer_server_ciphers on;
    ssl_protocols TLSv1 TLSv1.1 TLSv1.2; # not possible to do exclusive
    ssl_ciphers 'EDH+CAMELLIA:EDH+aRSA:EECDH+aRSA+AESGCM:EECDH+aRSA+SHA384:EECDH+aRSA+SHA256:EECDH:+CAMELLIA256:+AES256:+CAMELLIA128:+AES128:+SSLv3:!aNULL:!eNULL:!LOW:!3DES:!MD5:!EXP:!PSK:!DSS:!RC4:!SEED:!ECDSA:CAMELLIA256-SHA:AES256-SHA:CAMELLIA128-SHA:AES128-SHA';
    add_header Strict-Transport-Security max-age=15768000; # six month
```

For Apache:
```
SSLEngine On
SSLCertificateFile /etc/letsencrypt/live/your_domain.tld/fullchain.pem
SSLCertificateKeyFile /etc/letsencrypt/live/your_domain.tld/privkey.pem
# This is valid only for Apache 2.4.8 or later if using OpenSSL 1.0.2 or later
SSLOpenSSLConfCmd DHParameters /etc/letsencrypt/live/your_domain.tld/dhparam.pem
SSLProtocol All -SSLv2 -SSLv3
SSLHonorCipherOrder On
SSLCompression off
# Add six earth month HSTS header for all users...
Header set Strict-Transport-Security "max-age=15768000"
# If you want to protect all subdomains, use the following header
# ALL subdomains HAVE TO support HTTPS if you use this!
# Strict-Transport-Security: "max-age=15768000 ; includeSubDomains"
SSLCipherSuite 'EDH+CAMELLIA:EDH+aRSA:EECDH+aRSA+AESGCM:EECDH+aRSA+SHA384:EECDH+aRSA+SHA256:EECDH:+CAMELLIA256:+AES256:+CAMELLIA128:+AES128:+SSLv3:!aNULL:!eNULL:!LOW:!3DES:!MD5:!EXP:!PSK:!DSS:!RC4:!SEED:!ECDSA:CAMELLIA256-SHA:AES256-SHA:CAMELLIA128-SHA:AES128-SHA'
```

*Make sure to visit https://cipherli.st/ to get an updated SSL cipher list for your webserver.*

Setup autorenewal of all the certificates:
```
sudo crontab -e
30 3 * * 0 /opt/letsencrypt/letsencrypt-auto renew
35 3 * * 0 /bin/systemctl reload nginx
```

You're done!
