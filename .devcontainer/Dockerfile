FROM python:3.11-slim

# Install Java (required by Spark)
RUN apt-get update && apt-get install -y \
    default-jdk \
    curl \
    && rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME=/usr/lib/jvm/default-java

# Install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt