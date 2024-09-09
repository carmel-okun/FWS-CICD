# Use the official Nginx image from Docker Hub
FROM nginx:latest

# Copy custom Nginx configuration file (optional)
# COPY nginx.conf /etc/nginx/nginx.conf

# Copy static content to the Nginx default directory
COPY ./html /usr/share/nginx/html

# Expose port 80 for the Nginx service
EXPOSE 80

# Command to run Nginx
CMD ["nginx", "-g", "daemon off;"]
