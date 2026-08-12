# Use the official Microsoft Python devcontainer image as base
FROM mcr.microsoft.com/devcontainers/python:3.12

# Install additional system dependencies (if needed)
# RUN apt-get update && apt-get install -y <your-package>

# Set pip to use a faster mirror (optional)
ENV PIP_INDEX_URL=https://pypi.org/simple

# Copy requirements if they exist (user will mount their own)
# WORKDIR /workspace
RUN pip install pandas numpy matplotlib