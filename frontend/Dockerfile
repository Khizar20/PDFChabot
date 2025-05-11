# Use an official Nginx image as a parent image
FROM nginx:stable-alpine # Using stable-alpine for a small and secure image

# Optional: Remove the default Nginx welcome page.
# This ensures only your files are served from the root.
RUN rm -rf /usr/share/nginx/html/*

# Copy your static frontend files (HTML, CSS, JS, images, etc.)
# from the current directory (which will be the 'frontend' directory during the build context)
# to Nginx's default web server root directory.
COPY . /usr/share/nginx/html/

# Expose port 80 (this is the default port Nginx listens on)
EXPOSE 80

# Nginx will start automatically when the container runs.
# The base Nginx image already has the CMD to start Nginx.
