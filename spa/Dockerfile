# Use an official Node.js runtime as the base image.
FROM node:20-alpine

# Set the working directory to /app
WORKDIR /app

# Copy package.json and package-lock.json to leverage Docker cache
# and install dependencies first.
COPY package*.json ./

# Install project dependencies.
# The `npm install` command will be much faster on subsequent builds
# as long as package*.json files don't change.
RUN npm install

# Expose port 3000, which is the default for a React dev server.
EXPOSE 3000

# The command to start the development server.
# This will watch for file changes in the mounted volume and trigger a hot reload.
CMD ["npm", "start"]
