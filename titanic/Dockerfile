# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file first to leverage Docker's caching mechanism for dependencies
COPY requirements.txt /app/requirements.txt

# Install dependencies
RUN pip install --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

# Copy the rest of the local files (including the Titanic dataset and Python scripts) to the container
COPY . /app

# Set the entry point to run the Python script
CMD ["python", "titanic.py"]
