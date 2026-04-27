# consumer-service/Dockerfile
# Usa una imagen runtime moderna y mantenida para Java 17
FROM eclipse-temurin:17-jre-jammy

# Argumento para el JAR ejecutable generado por Spring Boot
ARG JAR_FILE=target/*SNAPSHOT.jar

# Directorio de trabajo
WORKDIR /app

# Copia el JAR
COPY ${JAR_FILE} app.jar

# No necesita exponer puerto si solo consume mensajes
# EXPOSE 8081

# Comando de ejecución
ENTRYPOINT ["java", "-jar", "app.jar"]