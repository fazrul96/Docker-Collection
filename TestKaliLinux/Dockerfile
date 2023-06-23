# FROM kalilinux/kali-linux-docker pull access denied for kalilinux/kali-linux-docker
FROM kalilinux/kali-rolling

# Update and install essential packages
RUN apt-get update && \
    apt-get install -y curl && \
    apt-get upgrade -y && \
    apt-get install -y \
    curl \
    git \
    vim \
    wget \
    net-tools \
    iputils-ping \
    nmap \
    sqlmap \
    nikto \
    dirb \
    hydra \
    john \
    hashcat \
    metasploit-framework \
    exploitdb \
    gobuster \
    python3-pip \
    && apt-get clean

# Install Docker Compose
RUN curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose \
    && chmod +x /usr/local/bin/docker-compose

# Configure Metasploit database
RUN service postgresql start && msfdb init

# Set default work directory
WORKDIR /root

# Set default command
CMD ["/bin/bash"]