FROM registry.access.redhat.com/ubi8/nodejs-16:latest

# Set the working directory
WORKDIR /opt/app-root/src

# Copy package files
COPY package*.json ./

# Remove old package-lock.json and install dependencies
RUN rm -f package-lock.json && npm install --omit=dev

# Copy application code
COPY . .

# Expose port
EXPOSE 8080

# Set environment variables
ENV NODE_ENV=production
ENV PORT=8080

# Start the application
CMD ["npm", "start"]