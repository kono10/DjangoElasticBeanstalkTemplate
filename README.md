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
~/DjangoElasticBeanstalkTemplate/myproject

❯ docker-compose up --build
```
