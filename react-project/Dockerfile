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

# Build the Vue.js application to the production mode to dist folder
RUN npm run build

# production stage
FROM nginx:stable-perl as production-stage
COPY --from=build-stage /app/build /usr/share/nginx/html

# Expose the port 8080
EXPOSE 8080

# Start Nginx to serve the application
CMD ["nginx", "-g", "daemon off;"]