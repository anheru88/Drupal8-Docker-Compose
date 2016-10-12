# Docker Compose: Drupal 8.2.1

Drupal development environment using [Docker Compose](https://docs.docker.com/compose/).


## Prerequisites

1. [Docker](http://docker.com)
  ```
  docker --version
  ```
2. [Docker Compose](https://docs.docker.com/compose/)
  ```
  docker-compose --version
  ```

## Usage:

1. Run `docker-compose build` please wait a few minutes, docker need download images, and build the new base images.

2. Run `docker-compose up -d` and create the new containers.

3. Run `docker ps` and see the list of containers running in your machine.

4. Visit [`http://localhost`](http://localhost) in your browser.

5. Configure your Drupal Site.

6. Enjoy.

## License

Licensed under the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT license](http://creativecommons.org/licenses/MIT/)

Copyright &copy; 2016+ [anheru88](https://github.com/anheru88)
