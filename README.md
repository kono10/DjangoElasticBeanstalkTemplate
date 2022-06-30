## Start up the django development server for local testing
* accessed from localhost:8001
```
❯ pwd
~/DjangoElasticBeanstalkTemplate/myproject

❯ docker build -f Dockerfile.dev -t djangodev .

❯ docker run -p 8001:8000 djangodev
```

## Start up production server (uses gunicorn and nginx) locally
* can add -D or --daemon command to the below to run in the background
* accessed from localhost
```
❯ pwd
~/DjangoElasticBeanstalkTemplate

❯ docker-compose up --build
```

## Todo
* add unit tests
  * unit tests failing during build bc environment doesn't have python packages installed
* upload docker containers to dockerhub



docker-compose -f docker-compose-dev.yml up --build                                                     ─╯
