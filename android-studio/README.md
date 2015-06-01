# Run Android Studio from a docker container

Clone the project somewhere in your machine and cd into the dockerfiles directory:

```bash
$ git clone https://github.com/reul/dockerfiles.git dockerfiles
$ cd dockerfiles
```

Build the docker image with Android Studio:

```bash
$ sudo docker build --rm --tag=android-studio android-studio
```

Then disable access control for the current X session:
 ```bash
 $ xhost +
 ```

Finally run the container:
```bash
$ sudo docker run -t -i \
    -e DISPLAY \
    -v /tmp/.X11-unix:/tmp/.X11-unix:ro \
    -v $HOME/.Xauthority:/home/developer/.Xauthority:ro \
    --net=host \
    --name android-studio \
    android-studio

```




