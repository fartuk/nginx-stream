# nginx-stream

RTMP stream processing server

## Server installation
### Build docker
```shell
docker build -t nginx-stream -f Dockerfile-nginx-stream .
```
### Run container
```shell
docker run -it -d -p 1935:1935 -v /home/user/ssd/nginx-stream:/workdir:rw nginx-stream
```

## Mobile app settings
Install app <https://play.google.com/store/apps/details?id=com.spynet.camon&hl=ru>

It is used to stream data from mobile camera to server by RTMP.

Configure live-streaming server:
```
server: rtmp://ip-addres:1935/cam1
stream: mystream
```

## Usage
Open <rtmp://ip-addres:1935/cam1/mystream> in browser or VLC to see live stream.

Video-files will be stored in the [data](data) folder
