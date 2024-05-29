# Use the official Python image from the Docker Hub
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /whisper

# Clone the repository from GitHub
RUN apt-get update && apt-get install -y git \
    && git clone https://github.com/openai/whisper.git .

# Install the requirements
RUN pip install --no-cache-dir -r requirements.txt

# Expose any ports the app is expecting in the environment
EXPOSE 8000

# Command to run the application
CMD ["python", "main.py"]
