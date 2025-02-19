# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json .
RUN npm install

# Copy the application files
COPY . .

# Expose port 3000 for communication
EXPOSE 3000

# Command to run the application
CMD ["node", "server.js"]
