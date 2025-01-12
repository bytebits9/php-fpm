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
- `8.4.2`, `8.4`, `8.4.2-cli`, `8.2-cli`
- `8.4.2-fpm`, `8.4-fpm`
- `8.3.14`, `8.3`, `8.3.14-cli`, `8.3-cli`
- `8.3.14-fpm`, `8.3-fpm`
- `8.2.26`, `8.2`, `8.2.26-cli`, `8.2-cli`
- `8.2.26-fpm`, `8.2-fpm`
- `8.1.30`, `8.1`, `8.1.30-cli`, `8.1-cli`
- `8.1.30-fpm`, `8.1-fpm`

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