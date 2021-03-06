# nginx-geoip2

[![dockeri.co](https://dockeri.co/image/jidckii/nginx-geoip2)](https://hub.docker.com/r/jidckii/nginx-geoip2)  
[![](https://images.microbadger.com/badges/image/jidckii/nginx-geoip2.svg)](https://microbadger.com/images/jidckii/nginx-geoip2 "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/jidckii/nginx-geoip2.svg)](https://microbadger.com/images/jidckii/nginx-geoip2 "Get your own version badge on microbadger.com")

Build based on official nginx and  [telize](https://github.com/jessfraz/dockerfiles/tree/master/telize)

IP database location in /usr/share/GeoIP  
 
For check:  
1. clone original git repo 
2. change `localhost` to `_`in file nginx.vh.default.conf
3. Run:  
`docker run --rm -it --name nginx-geoip2 --net host -v $PWD/nginx.vh.default.conf:/etc/nginx/conf.d/default.conf jidckii/nginx-geoip2:latest`  
Curl from host public ip:  
```
curl -I http://${you-host-or-ip}
```
example response:
```
HTTP/1.1 200 OK
...
x-geoip-continent_code: EU
x-geoip-country: Germany
x-geoip-country_code: DE
...
```
