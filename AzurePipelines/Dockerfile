# Use the specified Node.js base image
FROM node:19.7.0-alpine

# Set environment variable
ENV NODE_ENV=production

# Create a new directory and set permissions
RUN mkdir /labone \
    && chown node:node /labone

# Set working directory
WORKDIR /labone

# Set user to node
USER node

# Copy source files and change file ownership
COPY --chown=node:node . .

# Install npm packages
RUN npm install

# Expose port 3000
EXPOSE 3000

# Default command to run the application
CMD ["node", "src/index.js"]
