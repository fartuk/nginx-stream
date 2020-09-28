# nginx-stream
RTMP stream processing server

## Build docker
docker build -t nginx-stream -f Dockerfile-nginx-stream .

## Run container
docker run --rm -it -p 1935:1935 -v /home/user/ssd/nginx-stream:/workdir:rw nginx-stream
