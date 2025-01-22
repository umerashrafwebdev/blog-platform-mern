# Use an official Node.js runtime as the base image
FROM node:22

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json into the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React app for production
# RUN npm run build

# Use an Nginx server to serve the built files
FROM nginx:alpine
# COPY --from=0 /usr/src/app/build /usr/share/nginx/html

# Expose the port the frontend server runs on
EXPOSE 80

# Command to start Nginx
CMD ["nginx", "-g", "daemon off;"]