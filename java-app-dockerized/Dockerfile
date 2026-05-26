# Stage 1: Build (compile)
FROM openjdk:17-slim AS builder

WORKDIR /app

COPY HelloServer.java .
RUN javac HelloServer.java

# Stage 2: Runtime
FROM openjdk:17-jdk-slim

WORKDIR /app

# Copy all compiled class files (main + inner)
COPY --from=builder /app/*.class /app/

EXPOSE 8080

CMD ["java", "HelloServer"]