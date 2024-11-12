# Use the base image
FROM labani/terabox:latest

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file to the working directory
COPY requirements.txt .

# Install dependencies without caching and to avoid breaking system packages
RUN pip3 install --no-cache-dir --break-system-packages -r requirements.txt

# Copy the remaining application files to the container
COPY . .

# Specify the default command to run your application (adjust as necessary)
CMD ["bash", "start.sh"]
