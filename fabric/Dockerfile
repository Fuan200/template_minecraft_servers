FROM eclipse-temurin:17-jdk

WORKDIR /app
COPY . /app

COPY fabric-server-mc.1.20.1-loader.0.19.3-launcher.1.1.1.jar /app/fabric-server-launch.jar

ENTRYPOINT ["java", "-Xms4096M", "-Xmx5632M", "-jar", "/app/fabric-server-launch.jar", "nogui"]