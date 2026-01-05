# Use the official Jenkins LTS image as the base
FROM jenkins/jenkins:lts

# Switch to the root user to install system packages
USER root

# Update package lists and install Python 3, pip, and other necessary build tools
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    python3-venv \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# (Optional) Set Python 3 as the default 'python' executable via an alias or symlink if preferred, 
# but generally best practice is to use 'python3' and 'pip3' explicitly.

# Switch back to the 'jenkins' user (standard practice for security)
USER jenkins