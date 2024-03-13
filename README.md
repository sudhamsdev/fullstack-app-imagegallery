# FullStack App
## Specifications
- Docker Engine

### Note
- Update React and Springboot codes with Docker Host machine IP address to access application

## Launch PostgreSQL Database
- Build PostgreSQL Image
```
cd postgresql
docker image build -t <repository>:<tag> . [--no-cache]
```
- Launch PostgreSQL Container
```
docker container run -d --name postgresql -e POSTGRES_DB=xxxxx -e POSTGRES_USER=xxxxx -e POSTGRES_PASSWORD=xxxxx p5432:5432 <repository>:<tag>
```


## Setup springboot application
- Build Springboot Image
```
cd springboot
docker image build -t <repository>:<tag> . [--no-cache]
```
- Launch container from above build image
```
docker container run -d --name springboot -p8080:8080 <repository>:<tag>
```

## Setup React application
- Build React Image
```
cd react
docker image build -t <repository>:<tag> . [--no-cache]
```
- Launch container from above build image
```
docker container run -d --name reactapp -p8090:80 <repository>:<tag>
```
