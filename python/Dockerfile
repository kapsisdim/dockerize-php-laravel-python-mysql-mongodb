FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /python-scripts

# Copy the current directory contents into the container at /app
COPY . .

# Install any dependencies specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
