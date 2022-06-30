## Start up the django development server for local testing
* accessed from localhost:8001
```
❯ pwd
~/DjangoElasticBeanstalkTemplate/myproject

❯ docker build -f Dockerfile.dev -t djangodev .

❯ docker run -p 8001:8000 djangodev
```

## Start up production server (uses gunicorn and nginx) build and run docker containers locally
* can add -D or --daemon command to the below to run in the background
* accessed from localhost
```
❯ pwd
~/DjangoElasticBeanstalkTemplate

❯ docker-compose -f docker-compose-dev.yml up --build  
```

### File Index
* docker-compose-dev.yml -> test production infrastructure with local docker builds
* docker-compose.yml -> can run production infrastructure locally but pulls docker containers from dockerhub, is the the compose file used by AWS
* Dockerfile.dev -> run Django app locally with Django development server
