# Use the official Node.js image as the base image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json files to the container
COPY package*.json ./

# Install all dependencies (including devDependencies)
RUN npm install

# Install global tools like Nest CLI and nodemon
RUN npm install -g @nestjs/cli nodemon

# Copy the rest of the application code to the container
COPY . .

# Expose the port the app runs on
EXPOSE 4000

# Command to start the app in development mode
CMD ["npm", "run", "start:dev"]
