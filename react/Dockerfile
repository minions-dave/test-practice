# Use an official Node.js runtime as the base image
FROM node:lts-slim

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Build the React app for production
RUN npm run build

# Expose port 80 to the outside world
EXPOSE 80

# Define the command to run when the container starts
CMD [ "npx", "serve", "-s", "build", "-l", "80" ]
