# Creating the app


## Testing With Docker
```
> docker build -f Dockerfile.test -t apptest .                                                                                                                     ─╯

> docker run -p 8001:8000 apptest                                                                                                                                 ─╯
```


## Staring WSGI With Gunicorn
* can add -D or --daemon command to the below command to run in the background
```
❯ pwd
/myproject

❯ gunicorn --bind 0.0.0.0:8000 --workers=4 myproject.wsgi:application

[2022-06-17 13:44:47 -0500] [31652] [INFO] Starting gunicorn 20.1.0
[2022-06-17 13:44:47 -0500] [31652] [INFO] Listening at: http://0.0.0.0:8000 (31652)
[2022-06-17 13:44:47 -0500] [31652] [INFO] Using worker: sync
[2022-06-17 13:44:47 -0500] [31654] [INFO] Booting worker with pid: 31654
[2022-06-17 13:44:48 -0500] [31655] [INFO] Booting worker with pid: 31655
[2022-06-17 13:44:48 -0500] [31656] [INFO] Booting worker with pid: 31656
[2022-06-17 13:44:48 -0500] [31657] [INFO] Booting worker with pid: 31657

```






