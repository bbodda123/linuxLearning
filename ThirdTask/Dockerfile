# 1. Use OpenJDK 17 as the base image
FROM openjdk:17-jdk-slim

# 2. Set working directory
WORKDIR /app

# 3. Copy Maven wrapper and project files
COPY . .

# 4. Give execute permission to Maven wrapper
RUN chmod +x mvnw

# 5. Download The App Dependencies 
RUN ./mvnw package

# 6. Expose Spring Boot's default port
EXPOSE 8080

# 7. Run Spring Boot app using Maven wrapper
CMD ["./mvnw", "spring-boot:run"]
