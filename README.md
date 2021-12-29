# README #

Docker compose file for haproxy backed by lets encrypt certificates. The services talk to each other to share certificates.

### Setup ###

Expects the following persistent volumes:
$HOME/config/haproxy/haproxy - stores HA Proxy configuration files.
$HOME/config/haproxy/ssl - stores certificates from Let's encrypt including required keys used to sign and renew certificates.

Files required:
$HOME/config/haproxy/haproxy/haproxy.cfg - HA Proxy configuration file.
$HOME/config/haproxy/environments.txt - docker environment variables. This includes domains to issue SSLs for.

The haproxy.cfg and environments.txt should match to ensure all certificates are renewed and used.
