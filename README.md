# NginxProxy

If you need to develop web application inside your local environment (for example using Vagrant) and your application must be visible from the outside,
you can create proxy server on any cheap hosting (AWS micro instance) and make reverse tunnel to it.

There is an example of NGINX config file for proxy server. According to LUA script in this config, all requests started with /instances/vault/ will be
proxied to 9999 port. You have to create reverse tunnel from your local environment to receive this requests from 9999 to yours localhost:80.
```
ssh -i key.pem -R 9999:localhost:80 admin@XX.XXX.XXX.XX
```
