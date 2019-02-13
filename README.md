# nginx-geoip2

On docker hub: <https://hub.docker.com/r/jidckii/nginx-geoip2>

Build based on official nginx and  [telize](https://github.com/jessfraz/dockerfiles/tree/master/telize)

IP database location in /usr/share/GeoIP  
 
For check:  
Run:  
`docker run --rm -it --name nginx-geoip2 --net host jidckii/nginx-geoip2:latest`  
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
