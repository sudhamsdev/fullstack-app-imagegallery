FROM openjdk:18-alpine
LABEL maintainer="sudhams reddy duba<sudhams@visualpath.in>"
RUN apk add maven
COPY . /src
WORKDIR /src
RUN mvn clean install
EXPOSE 8080
CMD ["mvn", "spring-boot:run"] 
