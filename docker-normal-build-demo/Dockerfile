#using the argument 

ARG TAG=3.6.3-jdk-8

# select parent image 
FROM maven:${TAG}

# using the workdir 

WORKDIR /app

# copy the source tree and the pom.xml to our new container 
COPY .  .

# package our application code 
RUN mvn clean package 

# set the startup command to execute the jar 
CMD ["java", "-jar", "target/demo-0.0.1-SNAPSHOT.jar"]
