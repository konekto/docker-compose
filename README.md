# Docker Compose

This docker image installs docker-compose on top of the `docker` image.
This is very useful for CI pipelines, which leverage "Docker in Docker".

## Usage instructions for GitLab CI

You may use it like this in your `.gitlab-ci.yml` file.

```yaml
build:
  stage: build
  # set the image
  image: konekto/docker-compose:latest
  # use docker-compose commands 🛳
  script:
    - docker-compose down
    - docker-compose up --build
```
