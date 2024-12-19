#### Build & Push docker image

```bash
docker build -f Dockerfile -t siddhivinayaksk1/nginx-rp:latest .
docker push siddhivinayaksk1/nginx-rp:latest
```

To list docker image:

```bash
docker image ls
````

To remove docker image:

```bash
docker image remove --force <image name> 
```

#### Run docker image locally

```bash
docker run -it --rm -d -p 8080:80 --name web -e TARGET_SERVER=httpbin.org -e TARGET_SERVER_PORT=80 nginx/custom-proxy:latest
```

To list docker container:

```bash
docker container ls
```

To stop docker container:

```bash
docker container remove --force <container name>
```

