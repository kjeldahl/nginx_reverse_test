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
