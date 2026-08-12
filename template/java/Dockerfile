FROM mcr.microsoft.com/devcontainers/java:21

# Install Maven and Gradle
RUN apt-get update && apt-get install -y \
    maven \
    gradle \
    && apt-get clean && rm -rf /var/lib/apt/lists/*