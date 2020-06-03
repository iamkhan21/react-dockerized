### Development

#### Create Docker image 
`docker build -t dockerized-react:dev -f Dockerfile.dev .`

#### Run Docker container
UNIX:
```bash
docker run -it --rm -v ${PWD}:/app -v /app/node_modules -p 3000:3000 -e CHOKIDAR_USEPOLLING=true dockerized-react:dev
```

WINDOWS:
```bash
docker run -it --rm -v %cd%:/app -v /app/node_modules -p 3000:3000 -e CHOKIDAR_USEPOLLING=true dockerized-react:dev
```


---


### Production

#### Create Docker image 
`docker build -t dockerized-react:prod -f Dockerfile.prod .`

#### Run Docker container
```bash
docker run -it -p 80:80 dockerized-react:prod
```
