# PHP Docker Container Image

A lightweight PHP container image based on Alpine Linux, building with the Clang and LLVM. 
It supports multiple architectures and is ideal for both development and production environments.

## Quick reference
- **Image based on**: [alpine](https://hub.docker.com/_/alpine)
- **Supported architectures**: `linux/amd64`, `linux/arm64`
- **Maintained by**: [grmvoid](https://github.com/grmvoid)
- **Issues**: [https://github.com/grmvoid/docker-php/issues](https://github.com/grmvoid/docker-php/issues?q=)

## Usage
### Pull the Image
To get started, pull the specify a version PHP image:
```bash
  docker pull grmvoid/php:8.4.4
```

### Running a Container
You can run the PHP container interactively using the following command:
```bash
  docker run -it --name php -v /path/to/app:app grmvoid/php:8.4.4
```

### Running a PHP Script
To execute a PHP script inside the container:
```bash
  docker run --rm -v $(pwd):/app -w /app grmvoid/php:8.4.4 php script.php
```

### Using as a Base Image
You can extend this image in your `Dockerfile`:
```dockerfile
FROM grmvoid/php:8.4.4
WORKDIR /app
COPY . .
CMD ["php", "index.php"]
```

## Environment Variables
The php image uses several environment variables which are easy to miss.

| Variable      | Default Value | Description                               |
|---------------|---------------|-------------------------------------------|
| `PHPIZE_DEPS` |               | Dependencies required for PHP extensions  |

## LICENSE
This repository follows the [PHP License](https://www.php.net/license/). Individual dependencies may have their own licensing terms.

Additionally, the contents of this repository are licensed under the [MIT License](LICENSE).