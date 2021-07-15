FROM openjdk:11.0
RUN mkdir myapp
COPY app.jar ./myapp
WORKDIR ./myapp
EXPOSE 8080
VOLUME /myapp
ENTRYPOINT ["java", "-jar", "app.jar"]
