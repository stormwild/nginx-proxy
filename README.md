# Nginx Proxy Tutorial

## Create network

```
docker run -d -p 80:80 --name nginx-proxy --net nginx-proxy -v /var/run/docker.sock:/tmp/docker.sock jwilder/nginx-proxy
```

```
docker run -d --name blog --expose 80 --net nginx-proxy -e VIRTUAL_HOST=wpx.com wpx
```


## References

- [How to use Docker and Nginx to host multiple websites on one VPS](https://blog.ssdnodes.com/blog/tutorial-using-docker-and-nginx-to-host-multiple-websites/)

- [Set a local web development environment with custom Urls and HTTPS](https://medium.com/@francoisromain/set-a-local-web-development-environment-with-custom-urls-and-https-3fbe91d2eaf0)

- [Host multiple websites with HTTPS on a single server](https://medium.com/@francoisromain/host-multiple-websites-with-https-inside-docker-containers-on-a-single-server-18467484ab95)