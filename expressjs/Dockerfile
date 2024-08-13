# build stage
# Use the node image from official Docker Hub
FROM node:slim as build-stage


# set the working directory
WORKDIR /app

# Copy json files for dependences in the container
COPY package*.json .

# Install the project dependencies
RUN npm install

# Copy the rest of the project files to the container
COPY . .

# Expose the port 3000
EXPOSE 3000

# Start Nginx to serve the application
CMD ["node", "app.js"]