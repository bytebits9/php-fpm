## Quick reference
- **Image based on**:   
  [alpine](https://hub.docker.com/_/alpine)

- **Supported architectures**:    
  `linux/amd64`, `linux/arm64`

- **Maintained by**:  
  [grmvoid](https://github.com/grmvoid)

- **Where to file issues**:    
  [https://github.com/grmvoid/docker-php/issues](https://github.com/grmvoid/docker-php/issues?q=)

## Supported tags and respective `Dockerfile` links
- [`8.4.2`, `8.4`, `8.4.2-cli`, `8.4-cli`](https://github.com/grmvoid/docker-php/blob/834c92021be39dd01c9b77cb8d658ab522778f54/8.4/cli/Dockerfile)
- [`8.4.2-fpm`, `8.4-fpm`](https://github.com/grmvoid/docker-php/blob/834c92021be39dd01c9b77cb8d658ab522778f54/8.4/fpm/Dockerfile)
- [`8.3.15`, `8.3`, `8.3.15-cli`, `8.3-cli`](https://github.com/grmvoid/docker-php/blob/eb2075975c7701805dffb849c9999ff2d1b94b75/8.4/fpm/Dockerfile)
- [`8.3.15-fpm`, `8.3-fpm`](https://github.com/grmvoid/docker-php/blob/eb2075975c7701805dffb849c9999ff2d1b94b75/8.4/fpm/Dockerfile)
- [`8.2.27`, `8.2`, `8.2.27-cli`, `8.2-cli`](https://github.com/grmvoid/docker-php/blob/1dca4fbaafd7ff5539463598fa89989d52b5d646/8.4/fpm/Dockerfile)
- [`8.2.27-fpm`, `8.2-fpm`](https://github.com/grmvoid/docker-php/blob/1dca4fbaafd7ff5539463598fa89989d52b5d646/8.4/fpm/Dockerfile)
- [`8.1.31`, `8.1`, `8.1.31-cli`, `8.1-cli`](https://github.com/grmvoid/docker-php/blob/3f4100a5087e9da33a59ac2ab690e4c9c2dff172/8.4/fpm/Dockerfile)
- [`8.1.31-fpm`, `8.1-fpm`](https://github.com/grmvoid/docker-php/blob/3f4100a5087e9da33a59ac2ab690e4c9c2dff172/8.4/fpm/Dockerfile)

## How to usage this image

Create a `Dockerfile`
```Dockerfile
FROM grmvoid/php:8.4.1-cli
COPY . /app
WORKDIR /app
CMD [ "php", "./script.php" ]
```

Then, build and run the Docker image
```bash
docker build -t php-app 
```
```bash
  docker run -it --rm --name custom-app php-app
```
## Environment Variables

The php image uses several environment variables which are easy to miss.

| Variable      | Default Value | Description |
|---------------|---------------|-------------|
| `PHPIZE_DEPS` |               |             |

## LICENSE

View [license](https://www.php.net/license/) information for the software contained in this image.