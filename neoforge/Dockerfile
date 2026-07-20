FROM eclipse-temurin:17-jdk

WORKDIR /app
COPY . /app

RUN java -jar neoforge-20.2.93-installer.jar --installServer && \
    rm neoforge-20.2.93-installer.jar

ENTRYPOINT ["/app/run.sh"]
