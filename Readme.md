
# NGINX Distroless Docker Container

This project provides a lightweight, secure NGINX container image using Distroless and NGINX Unprivileged base images. It's designed to run NGINX in a minimal environment, which reduces the attack surface and minimizes the size of the image.

## Features

- **Security-focused**: Built on top of the NGINX Unprivileged and Distroless base images for enhanced security.
- **Minimalistic**: Includes only the necessary binaries, configuration files, and libraries required to run NGINX.
- **Permission Hardening**: Ensures proper permissions for NGINX cache and log directories.

## Getting Started

These instructions will get you a nginx container based on distroless running on your local machine for development and testing purposes.

### Prerequisites

Before you begin, ensure you have met the following requirements:

- Docker is installed on your machine. If not, follow the [Docker installation guide](https://docs.docker.com/get-docker/).

### Installing

Pull the image from the Docker repository:

```bash
docker pull distrolessdevops/nginx-distroless:latest
```

### Usage

Run the container using:

```bash
docker run -d -p 8080:8080 distrolessdevops/nginx-distroless:latest
```

This command will start the NGINX server listening on port `8080`.

#### Customizing NGINX Configuration

To use your custom NGINX configuration, mount your configuration file to `/etc/nginx/nginx.conf`:

```bash
docker run -d -p 8080:8080 -v ./nginx.conf:/etc/nginx/nginx.conf distrolessdevops/nginx-distroless:latest
```

## Contributing

We welcome contributions to this project! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/repository/tags).

## Authors

* **Micheal Choudhary** - *Initial work* - [Github](https://github.com/michealch)

See also the list of [contributors](https://github.com/michealch/nginx-distroless) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details. we take no resposibility for any damage happened, so use it at your own risk.

## Acknowledgments

- Inspiration.
- etc.
