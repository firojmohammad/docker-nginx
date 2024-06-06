# Use the official Alpine Linux image
FROM alpine:latest

# Install Nginx
RUN apk --no-cache add nginx

# Copy a simple Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Create document root directory if it doesn't exist
RUN mkdir -p /var/www/html

# Copy the index.html file to the Nginx document root
COPY index.html /var/www/html/

# Expose port 9000 to the host
EXPOSE 9000

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]

