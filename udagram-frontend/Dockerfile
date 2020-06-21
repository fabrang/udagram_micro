# Use NodeJS base image
FROM node:13

# Create app directory in Docker
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies in Docker
RUN npm install
RUN npm install -g @ionic/cli

# Copy app from local environment into the Docker image
COPY . .

# Set the API’s port number
EXPOSE 8100

# Define Docker’s behavior when the image is run
CMD ionic build
CMD ionic serve --host=0.0.0.0 --port=8100