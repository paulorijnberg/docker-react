# Specify base image
FROM node:15.4.0-alpine3.10

# Create a working directory, all the following events will be executed in the working directory
WORKDIR /usr/app

# Install dependencies
COPY ./package.json ./
RUN npm install
COPY ./ ./

# Default command
CMD ["npm", "start"]


