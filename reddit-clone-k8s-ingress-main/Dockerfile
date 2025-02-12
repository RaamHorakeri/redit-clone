# Use Node.js 19 with Alpine Linux for a small image
FROM node:19-alpine3.15

# Set working directory inside the container
WORKDIR /reddit-clone

# Copy package.json and package-lock.json first to take advantage of Docker's cache
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the necessary port
EXPOSE 3000

# Start the app
CMD ["npm", "run", "dev"]
