# SpringBoot Restful Docker Test

```Bash
mvn package
```

```Dockerfile
FROM openjdk版本
LABEL <key>=<value> ... maintainer="LexYuC"
# ADD SOURCE TO DOCKER IMAGE
ADD target/springboot-docker-demo-0.0.1-SNAPSHOT.jar springboot-docker-demo.jar
ENTRYPOINT ["java", "-jar", "springboot-docker-demo.jar"]
```

```BASH
# 切換至專案目錄下
docker build -t springboot-docker-demo:latest .

# 確認
docker images

# 執行
docker run -p 8082:8080 springboot-docker-demo
```

