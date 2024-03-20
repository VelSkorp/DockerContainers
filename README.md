# DockerContainers

DockerContainers is a repository containing Dockerfiles for various containerized applications.

## Usage

To build and run any of the applications contained in this repository using Docker, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/VelSkorp/DockerContainers.git
```
2. Navigate to the directory of the desired application (e.g., JenkinsWithDotnet6).

3. Build the Docker image:

```bash
docker build -t <image_name> .
```

Replace <image_name> with a name for your Docker image.

4. Run the Docker container:

```bash
docker run -d -p <host_port>:<container_port> <image_name>
```

Replace <host_port> with the port on your host machine that you want to map to the container's port, and <container_port> with the port specified in the application's Dockerfile.

5. Access the application through a web browser or other appropriate client using the specified host and port.

## Contributing

Contributions to this repository are welcome. If you have improvements or additional Dockerfiles for other applications, feel free to submit a pull request.

## License

This repository is licensed under the MIT License.
