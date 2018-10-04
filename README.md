# docker-pipeline-php

A Docker image for Phing based PHP 7.2 projects, conceived mainly for Bitbucket Pipelines (with git support).

### bitbucket-pipeline.yml

```yaml
image: marcandreappel/docker-pipeline-php:latest

pipelines:
  branches:
    master:
    - step:
        script:
        - curl -so phing.phar https://www.phing.info/get/phing-latest.phar
        - php phing.phar -f "build.xml" build
```

Phing needs to be downloaded inside the script part.
