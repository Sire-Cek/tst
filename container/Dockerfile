# Test web app that returns the name of the host/pod/container servicing req
FROM node:current-alpine

LABEL org.opencontainers.image.title="Ucim se Docker!" \
      org.opencontainers.image.description="Web server jako priklad" \
      org.opencontainers.image.authors="cracked"

# Create directory in container image for app code
RUN mkdir -p /usr/src/app

# Copy app code (.) to /usr/src/app in container image
COPY . /usr/src/app

# Set working directory context
WORKDIR /usr/src/app

# Install dependencies from package.json
RUN npm install

# Command for container to execute
ENTRYPOINT [ "node", "app.js" ]
