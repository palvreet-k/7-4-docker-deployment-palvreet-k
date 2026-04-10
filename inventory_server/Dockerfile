# Start from an existing base image (Node.js 20 on Alpine Linux)
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy dependency files first (enables layer caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app listens on
EXPOSE 3000

# The command that runs when the container starts
CMD ["node", "server.js"]