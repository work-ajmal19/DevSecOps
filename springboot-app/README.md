# Springboot App (Demo)

Simple Spring Boot demo application generated for testing.

Running locally (using the local toolchain created in this repo):

```bash
cd springboot-app
export JAVA_HOME=$PWD/.local-jdk
export PATH=$JAVA_HOME/bin:$PWD/.local-maven/bin:$PATH
mvn -Dmaven.repo.local=$PWD/.m2 clean package -DskipTests
java -jar target/springboot-app-0.0.1-SNAPSHOT.jar
```

Endpoint:

- GET / -> Hello message (http://localhost:8080/)

Build Docker image:

```bash
docker build -t springboot-app:latest .
docker run -p 8080:8080 springboot-app:latest
```

Notes:

- The repo includes a local JDK (`.local-jdk`) and Maven (`.local-maven`) extraction workflow used to build in restricted environments.
