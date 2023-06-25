# Use the official Node.js image as the base image
FROM node:14

# Set the working directory in the container
WORKDIR /app

# Copy the project files and directories to the container
COPY . .

# Install dependencies
RUN npm install

# Build the React app
RUN npm run build

# Expose port 3000
EXPOSE 3000

# Set the command to run the React app
CMD ["npm", "start"]