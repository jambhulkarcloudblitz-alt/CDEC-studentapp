FROM maven:3.8.5-openjdk-17

COPY . /app
WORKDIR /app

RUN mvn clean package 
EXPOSE 8080
WORKDIR /app/target

CMD ["java", "-jar","student-registration-backend-0.0.1-SNAPSHOT.jar"]

