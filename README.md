# Docker Collection

This repository contains a collection of Docker configurations for different purposes. Each folder represents a specific Docker configuration.

## Table of Contents

- [TestKaliLinux](#testkalilinux)
- [TestUbuntu](#testubuntu)

## TestKaliLinux

This Docker configuration sets up a Kali Linux environment with additional tools and configurations commonly used in penetration testing and security assessments.

### Usage

To build and run the TestKaliLinux container, follow these steps:

1. Clone this repository:

   ```shell
   git clone https://github.com/your-username/your-repo.git
   ```

2. Navigate to the `TestKaliLinux` folder:

   ```shell
   cd TestKaliLinux
   ```

3. Build the Docker image:

   ```shell
   docker build -t test-kali-linux .
   ```

4. Run the Docker container:

   ```shell
   docker run -d --name test-kali test-kali-linux
   ```

5. Access the running container:

   ```shell
   docker exec -it test-kali bash
   ```

   You should now be inside the Kali Linux environment and can start using the installed tools.

## TestUbuntu

This Docker configuration sets up an Ubuntu environment with additional packages and configurations.

### Usage

To build and run the TestUbuntu container, follow these steps:

1. Clone this repository:

   ```shell
   git clone https://github.com/your-username/your-repo.git
   ```

2. Navigate to the `TestUbuntu` folder:

   ```shell
   cd TestUbuntu
   ```

3. Build the Docker image:

   ```shell
   docker build -t test-ubuntu .
   ```

4. Run the Docker container:

   ```shell
   docker run -d --name test-ubuntu-container test-ubuntu
   ```

5. Access the running container:

   ```shell
   docker exec -it test-ubuntu-container bash
   ```

   You should now be inside the Ubuntu environment and can start working with it.

## Contributing

If you would like to contribute to this Docker collection, feel free to submit a pull request.
