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

```bash
docker image rm myapp4
docker image rm myapp5 -f # force
docker container rm myapp_c1 myapp_c2
```

```bash
docker system prune -a # delete everything (images, containers, volumes)
```

```bash
docker build -t myapp:v1 . # tags / version
docker run --name myapp_c -p 4000:4000 myapp:v1
```

```bash
docker start -i myapp_c # -i (interactive)
```

```bash
docker build -t myapp:nodemon .
docker run --name myapp_c_nodemon -p 4000:4000 --rm myapp:nodemon # temporary container
docker run --name myapp_c_nodemon -p 4000:4000 --rm -v C:\Users\Ekomobong\Documents\pro\docker-crash-course\api:/app -v /app/node_modules myapp:nodemon # temp. container + volumes
```
