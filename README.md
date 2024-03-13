# Containrization of Java fullstack application
## Specifications
- Docker Engine
- Docker Compose

## Springboot code changes
- Update application.properties file(Path --> springboot/src/main/resources/) with PostgreSQL DB details
```
spring.datasource.url=jdbc:postgresql://<DockerHostIP>:<PORT-FARWARD>/pokemon
spring.datasource.username=postgres
spring.datasource.password=1234
```

## React code changes
- Update main.jsx file(Path --> react/src/main.jsx) with Sprintboot application endpoint
```
axios.defaults.baseURL = 'http://<DockerHostIP>:<PORT-FARWARD>';
```

## Execute below command to spingup applications from path of the compose file
```
docker compose up -d
```

## Cleanup activity
```
docker compose down --rmi all -v
```
