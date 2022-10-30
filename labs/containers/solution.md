# Lab Solution

Search for `java` on Docker Hub and the official image is the top hit.

You might start by downloading the Java package:

```
docker pull java:9-jdk
```

Run a container to check the Java version:

```
docker run java:9-jdk java -version
```

And then the JRE build for Slim is the smallest:

```
docker pull java:9-jre-slim
```

```
docker image ls java
```

> 9-jdk is around 600MB; 9 JRE is 286MB *but* both are more than 4 years old...

## Using OpenJDK

The official Java page on Docker Hub is actually a redirect to the OpenJDK package, which is an open-source Java runtime.

But the `java` package is not the same as `openjdk` - and you should use `openjdk` because it's more up-to-date:

```
docker pull openjdk
docker pull openjdk:9-jre-slim
```

The default image tag is much more recent, and both images are smaller:

```
docker image ls openjdk
```
___
> Back to the [exercises](README.md).