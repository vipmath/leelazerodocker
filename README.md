# leelazer odocker
Leela Zero Dockerfile

Compile Leela-Zero in a docker (without GPU)

sabaki can use and call from docker like any other GTP
(docker exec or run)

```
docker
run -i --rm leelazero -g --noponder
time_settings 0 30 1;
```

![sabaki](images/sabaki.png "Sabaki")
