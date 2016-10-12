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

  ![img_1](https://github.com/anheru88/Drupal8-Docker-Compose/blob/master/images/image_1.png?raw=true)

2. Run `docker-compose up -d` and create the new containers.

  ![img_2](https://github.com/anheru88/Drupal8-Docker-Compose/blob/master/images/image_2.png?raw=true)

3. Run `docker ps` and see the list of containers running in your machine.

  ![img_3](https://github.com/anheru88/Drupal8-Docker-Compose/blob/master/images/image_3.png?raw=true)

4. Visit [`http://localhost`](http://localhost) in your browser.

  ![img_4](https://github.com/anheru88/Drupal8-Docker-Compose/blob/master/images/image_4.png?raw=true)

5. Configure your Drupal Site.

  ![img_5](https://github.com/anheru88/Drupal8-Docker-Compose/blob/master/images/image_5.png?raw=true)

6. Be sure the name of the machine its same the `docker ps` list like this: `nube_db_1`

8. By default the password of the database is `root`, and the database name is `drupal8`, if you need change this, only go to `docker-compose.yml` file and edit.

7. Enjoy.

  ![img_6](https://github.com/anheru88/Drupal8-Docker-Compose/blob/master/images/image_6.png?raw=true)

## License

Licensed under the incredibly [permissive](http://en.wikipedia.org/wiki/Permissive_free_software_licence) [MIT license](http://creativecommons.org/licenses/MIT/)

Copyright &copy; 2016+ [anheru88](https://github.com/anheru88)
