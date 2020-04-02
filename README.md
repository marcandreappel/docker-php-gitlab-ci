# PHP 7.4 Docker image for GitLab CI

A Docker image for PHP 7.4 projects (like Laravel).

## Usage

As the Docker image is automatically build on Docker Hub, you can use it straight in your pipeline:

```yaml
image: 'marcandreappel/docker-php-gitlab-ci:latest'

cache:
  paths:
    - vendor/
    - node_modules/

before_script:
  - composer install

...
```
