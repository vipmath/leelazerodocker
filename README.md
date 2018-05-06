# leelazer odocker
Leela Zero Dockerfile

## Create Image with leelaz_dockerfile.txt

```
docker build -f leelaz_dockerfile.txt .
```
You probably want to rename it to leelazero
```
docker images
docker tag [id of leelazero docker] leelazero:latest
```


## 
Compile Leela-Zero in a docker (without GPU)

sabaki can use and call from docker like any other GTP
(docker exec or run)

```
docker
run -i --rm leelazero -g --noponder
time_settings 0 30 1;
```

![sabaki](images/Screen%20Shot%202018-03-25%20at%2022.27.47.png "Sabaki")
