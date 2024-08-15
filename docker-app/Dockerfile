# Use an official node image as a base
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React app for production
RUN npm run build

# Serve the app with a simple static server
RUN npm install -g serve
CMD ["serve", "-s", "build"]

# Expose the port on which the app will run
EXPOSE 3000
