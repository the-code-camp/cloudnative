# Lab Solution

Search for `java` on Docker Hub and the official image is the top hit.

The official Java page on Docker Hub is actually a redirect to the OpenJDK package, which is an open-source Java runtime. But the `java` package is not the same as `openjdk` - and you should use `openjdk` because it's more up-to-date:

```
docker pull openjdk:9-jdk
```

Run a container to check the Java version:

```
docker run openjdk:9-jdk java -version
```

And then the JRE build for Slim is the smallest:

```
docker pull openjdk:9-jre-slim
```

```
docker image ls java
```

> 9-jdk is around 790MB; 9 JRE is 243MB *but* both are more than 6 years old...

```
docker image ls openjdk
```
___
> Back to the [exercises](README.md).