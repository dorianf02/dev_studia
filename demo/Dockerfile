# uycie obrazu z openjdk v17
FROM openjdk:17-jdk-slim

# katalog roboczy
WORKDIR /app

#skopiowanie plikow projektu do kontenera 
COPY . /app

# skopiowanie i zbudowanie projektu za pomoca mavena
RUN apt-get-update && apt-get install -y maven && \ mvn clean package -DskipeTests

# eksport na port 8080
EXPOSE 8080

#uruchomienie aplikacj spring-bootowej
CMD ["java", "jar", "target/demo-0.0.1-SNAPSHOT.jar"]
