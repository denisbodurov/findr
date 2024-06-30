![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-blue?logo=postgresql) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.1-brightgreen?logo=spring) ![React Native](https://img.shields.io/badge/React%20Native-0.74.2-blue?logo=react)
# Finder
## Required Installations
1. PostgreSQL 16
2. Java 17
3. Maven
4. NodeJs

## Starting PostgreSQL
To start the project, you need to initialize a database named "hackathon".
```sh
sudo -u postgres psql 
CREATE DATABASE hackathon; 
```

## Starting Spring
To run the project, you need to set the necessary database connection parameters. They can be found in the file: "src/main/resources/application.yml".
```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/hackathon
    username: username
    password: password
    driver-class-name: org.postgresql.Driver
```

Starting the Spring part of the project:
```sh
mvn spring-boot:run -Dspring-boot.run.jvmArguments="-server -XX:+TieredCompilation -XX:TieredStopAtLevel=4 -XX:+UseParallelGC -Xms512m -Xmx1024m"
```

## Starting React Native
To start the project, you need to initialize all dependencies in Node.
```sh
npm install
```

To set the endpoint paths, you need to edit the file: "client/.env".
```env
EXPO_PUBLIC_HOST=http://{ip}:{port}
```

Starting the React Native part of the project:
```sh
npm start
```
