# OpenVPN for Docker on Alpine

Quick instructions: see https://github.com/jpetazzo/dockvpn


Specific for alpine :

```bash
CID=$(docker run -d --privileged -p 1194:1194/udp firdavsich/alpinevpn)
docker run -t -i -p 8080:8080 --volumes-from $CID firdavsich/alpinevpn serveconfig
```
