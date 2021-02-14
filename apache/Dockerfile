# Base OS image to be used
FROM debian:stable-slim

# File Author / Maintainer
LABEL author="Wellington Ozorio"
LABEL version="1.0.0"

# Update the repository sources list
RUN apt update && \
    apt install -y apache2 && \
    apt clean

# Copy custom index.html file
COPY index.html /var/www/html/

# Expose Apache on port 80
EXPOSE 80

# Start Apache as a daemon in foreground mode
CMD ["apachectl", "-D", "FOREGROUND"]
