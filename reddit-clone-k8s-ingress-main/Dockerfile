# Use Node.js 18 (stable version) with Alpine Linux for a small image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /reddit-clone

# Copy package.json and package-lock.json separately to install dependencies first
COPY ./package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the necessary port
EXPOSE 3000

# Start the app
CMD ["npm", "run", "dev"]
