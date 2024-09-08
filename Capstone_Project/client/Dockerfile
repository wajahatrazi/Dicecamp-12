# Use official Python slim image for reduced size
FROM python:3.9.18-slim-bullseye

# Set working directory inside the container
WORKDIR /app

# Copy the Python script and requirements into the container
COPY client.py client.py
COPY requirements.txt requirements.txt

# Install dependencies from the requirements file
RUN pip install -r requirements.txt

# Set up a volume for storing client data
VOLUME /clientdata

# Run the client application using Uvicorn (Python ASGI server)
CMD ["python", "client.py"]
