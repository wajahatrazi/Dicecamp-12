# Containerizing WordPress Server & MySQL DB using Docker Compose in AWS EC2

## Architecture

<p align="center">
  <img src="Architecture Design.png" alt="Architecture Design">
</p>


## Setup: Ubuntu Server

<p align="center">
  <img src="image.png" alt="Ubuntu Server">
</p>

- SSH into the EC2 VM using your local machine:
- Go to the directory where your .pem file related to your EC2 instance is situated.
- Give it permissions with:
     ```
     chmod 400 <your-key-file>.pem
     ```
- SSH into the instance using:
     ```
     ssh -i <pem file> <username>@<Public IP>
     ```

- Update and upgrade the EC2 instance:
    ```
     sudo apt update && sudo apt upgrade -y
     ```

To reboot the EC2 instance, do it from the AWS Management Console.

## Installation: Docker & Docker-compose

- Install curl:
    ```
    sudo apt install curl
    ```

- Add Docker’s official GPG key:
    ```
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    ```

- Add Docker repository for Ubuntu:
    ```
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    ```

- Install Docker:
    ```
    sudo apt-get install docker-ce
    ```

- Install Docker Compose:
    ```
    sudo apt install docker-compose
    ```

- Add current user to Docker group:
    ```
    sudo usermod -aG docker $USER
    ```

- Check Docker versions:
    ```
    docker --version
    docker-compose --version
    ```

- Log out and back in again after adding yourself to the Docker users group before continuing.

- Restart Docker service if needed:
    ```
    sudo systemctl restart docker
    ```

## Configuration: WordPress in Docker


- Create a directory for WordPress:
    ```
    mkdir wordpress-docker
    cd wordpress-docker
    ```

- Edit docker-compose.yml:
    ```
    vi docker-compose.yml
    ```

- After editing, save and exit the editor.

- Start containers with Docker Compose:
    ```
    docker-compose up -d
    ```

- Access your WordPress server using the public IP or domain in your web browser.

## Access WordPress

- You should be redirected to the WordPress initial setup page. Verify containers are running:

| CONTAINER ID   | IMAGE      | COMMAND                | CREATED        | STATUS        | PORTS                               | NAMES                      |
|----------------|------------|------------------------|----------------|---------------|-------------------------------------|-----------------------------|
| bc8c896ca511   | wordpress  | "docker-entrypoint.s…" | 5 minutes ago  | Up 5 minutes  | 0.0.0.0:80->80/tcp, :::80->80/tcp   | wordpress_wordpress_1       |
| 28d93e3efc62   | mysql      | "docker-entrypoint.s…" | 5 minutes ago  | Up 5 minutes  | 3306/tcp, 33060/tcp                 | wordpress_db_1             |


### Open http://server-ip in your web browser.

<p align="center">
  <img src="image-1.png" alt="WordPress Setup Page" width="1000">
</p>


## References Websites

- Upcloud.com
- Stackoverflow.com