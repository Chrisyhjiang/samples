# Stage 1: Build the Angular app
FROM node:20-alpine AS builder

# Create and change to the app directory
WORKDIR /app

# Copy application dependency manifests to the container image
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the local code to the container image
COPY . .

# Build the Angular app
ARG SOCKET_IO_URL
RUN sed -i "s|SOCKET_IO_URL: ''|SOCKET_IO_URL: '${SOCKET_IO_URL}'|g" src/environments/environment.prod.ts
RUN npm run build -- --configuration production

# Stage 2: Serve the Angular app with Caddy
FROM caddy:2-alpine AS server

# Copy the built Angular files to the Caddy static file directory
COPY --from=builder /app/dist/frontend /usr/share/caddy

# Copy the Caddyfile
COPY Caddyfile /etc/caddy/Caddyfile

# Run Caddy with the Caddyfile configuration
CMD ["caddy", "run", "--config", "/etc/caddy/Caddyfile", "--adapter", "caddyfile"]
