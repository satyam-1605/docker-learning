# Use an official Node.js runtime as a parent image
FROM node:26-slim

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json first to leverage Docker's build cache
COPY package.json ./

# Install package dependencies
RUN npm install --only=production

# Copy the rest of the application code
COPY app.js ./

# Make port 3000 available to the world outside this container
EXPOSE 3000

# Run the app when the container launches
CMD ["node", "app.js"]
