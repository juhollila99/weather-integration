# How to build and run a Camel application

This project was generated using [Camel Jbang](https://camel.apache.org/manual/camel-jbang.html). Please, refer to the online documentation for learning more about how to configure the export of your Camel application.

This is a brief guide explaining how to build, "containerize" and run your Camel application.

## Build the Maven project (JVM mode)

```bash
./mvnw clean package
```

The application could now immediately run:

```bash
java -jar targetquarkus-appquarkus-run.jar
```

## Create a Docker container (JVM mode)

You can create a container image directly from the `src/main/docker` resources. Here you have a precompiled base configuration which can be enhanced with any further required configuration.

```bash
docker build -f src/main/docker/Dockerfile -t harkkatyo:1.0.0 .
```

Once the application is published, you can run it directly from the container:

```bash
docker run -it harkkatyo:1.0.0
```

## Build the Maven project (Native mode)

```bash
./mvnw package -Dnative
```

Native compilation can last a few minutes to complete. Once done, the application could immediately run:

```bash
./harkkatyo-1.0.0-runner
```

## Create a Docker container (Native mode)

You can create a container image directly from the `src/main/docker` resources. Here you have a precompiled base configuration which can be enhanced with any further required configuration.

```bash
docker build -f src/main/docker/Dockerfile.native -t native-harkkatyo:1.0.0 .
```

Once the application is published, you can run it directly from the container:

```bash
docker run -it native-harkkatyo:1.0.0
```
