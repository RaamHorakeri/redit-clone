# Use Node.js 18 with Alpine for a smaller image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json first to leverage Docker caching
COPY package*.json ./

# Install dependencies using npm ci for reproducible builds
RUN npm ci --omit=dev

# Copy the rest of the application files
COPY . .

# Expose the necessary port
EXPOSE 3000

# Use a non-root user for security
RUN adduser -D appuser
USER appuser

# Start the application
CMD ["npm", "run", "dev"]
