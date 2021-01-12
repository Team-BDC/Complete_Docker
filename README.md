# mysql-django 연동 추가사항
django-app 컨테이너에 attach해서 해줘야할 게 있음

python3 manage.py makemigrations
python3 manage.py migrate
python3 manage.py createsuperuser

# docker-demo
A Docker - composer example that provides a Django, Flask, Java, Redis, Elasticsearch, MySQL, Postgres, and Mongo container

# How to use a docker and composer
---
## Docker Prerequisites:
- Windows
https://docs.docker.com/docker-for-windows/install/
- Mac
https://docs.docker.com/docker-for-mac/install/


### 1. git clone
```
git clone https://github.com/Team-BDC/Complete_Docker
```

### 2. docker compose build and up 
```
cd new_Docker
(docker-compose.yml과 동일경로)

$ docker-compose build
...
Successfully built a597836853da
```

# Let’s run the API using docker
## Let’s build the docker image
```
docker-compose build
```

## Docker compose up with all associated docker compose services
```
$ docker-compose up
```
#### Note:
If you prefer to use a daemon mode, Let’s run the above command in the background:
```
$ docker-compose up -d
```

### 1. Django Python application
```
http://localhost:8000
```

### 2. React application
```
http://localhost:82
```

#### If you want to build/run a specific application
> ```
> docker-compose build <custom service>
> docker-compose run <custom service>
> 
> i.e. 
> docker-compose build nodejs_app
> docker-compose run nodejs_app
> ```

---
## How to use Redis, MySQL
### 1. Redis
https://redis.io/topics/rediscli
```
$ redis-cli -h localhost -p 6379
localhost:6379> exit
$ redis-cli ping
PONG
```

### 2. MySQL
https://www.mysql.com/products/workbench/
```
mysql -h localhost -p 3306 -u root -p1234
ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)

But, you may not be able to connect via command line.
Please use workbench
```


```
# newDocker
