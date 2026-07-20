FROM eclipse-temurin:17-jdk

WORKDIR /app

COPY quilt-installer-0.15.0.jar /app/quilt-installer-0.15.0.jar

RUN java -jar quilt-installer-0.15.0.jar install server 1.20.1 --download-server 

WORKDIR /app/server

COPY . /app/server/

WORKDIR /app/server

ENTRYPOINT ["java", "-Xms4096M", "-Xmx5632M", "-jar", "quilt-server-launch.jar", "nogui"]
