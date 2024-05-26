# Use the official Node.js image from the Docker Hub as the base image
FROM node:14

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if available) to the working directory
COPY package*.json ./

# Install npm version compatible with Node.js 14
RUN npm install -g npm@6

# Install the dependencies specified in package.json
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port the application will run on
EXPOSE 3000

# Define the command to run the application
CMD ["node", "src/index.js"]
