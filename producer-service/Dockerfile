# producer-service/Dockerfile
# Usa una imagen runtime moderna y mantenida para Java 17
FROM eclipse-temurin:17-jre-jammy

# Argumento para el JAR ejecutable generado por Spring Boot
ARG JAR_FILE=target/*SNAPSHOT.jar

# Establece el directorio de trabajo
WORKDIR /app

# Copia el JAR construido a la imagen
COPY ${JAR_FILE} app.jar

# Expone el puerto de la aplicación
EXPOSE 8080

# Comando para ejecutar la aplicación
ENTRYPOINT ["java", "-jar", "app.jar"]