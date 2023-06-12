# Use an official Node.js image as the base image
FROM node:16-alpine

# Set the working directory in the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the project dependencies
RUN npm install

# Copy the project files to the container
COPY . .

# Expose the port that the Vue app will run on
EXPOSE 3000

# Define the command to run the Vue app
CMD ["npm", "start"]
