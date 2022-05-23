This is an example of a nginx reverse proxy using
self signed certificates in combination with 
docker compose.

It is primarily a simple demonstration of a configuration
that can be used in a development environment.

INSTALLATION
------------

brew bundle # To install mkcert

mkcert -install # Install mkcert root certificate
mkdir certs
mkcert -cert-file certs/site12.local.pem -key-file certs/site12.local-key.pem site1.localhost site2.localhost

docker-compose up

Goto https://site1.localhost and https://site2.localhost and be greeted
by nginx and apache.

RESOURCES
---------

https://blog.amosti.net/local-reverse-proxy-with-nginx-mkcert-and-docker-compose/
https://stackoverflow.com/questions/51399883/adding-ssl-certs-to-nginx-docker-container
https://gist.github.com/eloypnd/5efc3b590e7c738630fdcf0c10b68072
https://www.acunetix.com/blog/articles/tls-ssl-cipher-hardening/
https://www.techrepublic.com/article/how-to-create-locally-signed-ssl-certificates-with-mkcert/
https://www.bogotobogo.com/DevOps/Docker/Docker-Compose-Nginx-Reverse-Proxy-Multiple-Containers.php
