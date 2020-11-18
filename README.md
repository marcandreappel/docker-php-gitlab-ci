# PHP 7.4 Docker image for GitLab CI

![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/marcandreappel/docker-php-gitlab-ci?logo=docker&logoColor=%23fff&style=for-the-badge)
![Docker Image Size (latest semver)](https://img.shields.io/docker/image-size/marcandreappel/docker-php-gitlab-ci?logo=ubuntu&logoColor=%23fff&sort=semver&style=for-the-badge)

An optimized docker image for PHP 7.4 projects (like Laravel) and useful on GitLab CI for debugging and unit testing.

## Usage

As the Docker image is automatically build on Docker Hub, you can use it right in your pipeline:

```yaml
image: 'marcandreappel/docker-php-gitlab-ci:release-2' # or :latest

cache:
  paths:
    - vendor/
    - node_modules/

before_script:
  - composer install

...
```

