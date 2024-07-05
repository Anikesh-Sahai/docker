# building the java file is little diffrent first we create a jar file and then we create entrypoint

# Build a JAR File
FROM maven:3.8.2-jdk-8-slim AS stage1
#mavinf is similar to alpine stage 1 is giving name we can give any name
WORKDIR /home/app
COPY . /home/app/
RUN mvn -f /home/app/pom.xml clean package
# pom.xml is the place where all the dependencied are added like package.json

# Create an Image
FROM openjdk:8-jdk-alpine
EXPOSE 5000
COPY --from=stage1 /home/app/target/hello-world-java.jar hello-world-java.jar
ENTRYPOINT ["sh", "-c", "java -jar /hello-world-java.jar"]
