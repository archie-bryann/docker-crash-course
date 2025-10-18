# docker-crash-course

All course files for the Docker Crash Course tutorial on the Net Ninja site &amp; YouTube channel.

```bash
cd api
docker build -t myapp . # . is location of Dockerfile
```

```bash
docker images
docker run --name myapp_c1 myapp
docker ps # running
docker stop myapp_c1
docker run --name myapp_c2 -p 4000:4000 -d myapp
docker ps -a # all
docker start myapp_c2
```
