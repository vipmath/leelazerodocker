# Leela Zero - Dockerfile & Run Instructions for Sabaki

## Create Image with leelaz_dockerfile.txt

By using the `--no-cache`, docker will fetch the latest network weights. You can re-run the command if you want to have the weights updated again.

```
docker build --no-cache -f leelaz_dockerfile.txt .
```

You probably want to rename it to leelazero

```
docker images
docker tag [id of leelazero docker] leelazero:latest
```

## Configure Sabaki to use Leela-Zero from docker

`Engines` > `Manage Engines` and use the following settings; 

```
docker
run -i --rm leelazero -g --noponder
time_settings 0 30 1;
```

docker supports mounts, which can be used to save the logfile;

```
docker
run -i --rm  -v /Users/leesedol/Downloads:/Downloads leelazero -g --noponder -l /Downloads/log_leela_zero_game.txt
time_settings 0 30 1;
```

![sabaki](images/Screen%20Shot%202018-03-25%20at%2022.27.47.png "Sabaki")
