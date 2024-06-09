# We need node 16
FROM node:16

EXPOSE 5000

WORKDIR /usr/src

RUN apt-get update && apt-get install -y curl

# Get and install node.js
RUN curl -sL https://deb.nodesource.com/setup_16.x && apt install -y nodejs

# Copy all of the source code
COPY . .

# Configure api path run
ENV REACT_APP_BACKEND_URL="http://localhost:8080"

# Install and build npm, install serve package 
RUN npm install && npm run build && npm install -g serve

# And finally the commands to run the application
CMD ["serve", "-s", "-l", "5000", "build"]
