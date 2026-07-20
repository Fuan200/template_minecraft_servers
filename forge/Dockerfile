FROM eclipse-temurin:17-jdk

WORKDIR /app
COPY . /app

RUN java -jar forge-1.20.1-47.4.10-installer.jar --installServer && \
    rm forge-1.20.1-47.4.10-installer.jar

ENTRYPOINT ["/app/run.sh"]
