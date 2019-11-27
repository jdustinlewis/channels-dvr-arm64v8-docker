# channels-dvr-arm64v8-docker
Dockerfile for channels-dvr on arm64v8
Built to use with LibreElec on a Rock64

## Example build:
```
cd jdustinlewis/channels-dvr-arm64v8-docker
docker build -t jdustinlewis/channels-arm64v8:latest -t jdustinlewis/channels-arm64v8:tve tve/
```

## Example run:
```
docker run -dit --restart always -p 8089:8089 --mount type=bind,source=$CHANNELS_DVR_FOLDER,target=/channels-dvr --name channels-dvr jdustinlewis/channels-arm64v8:tve
```

## Bugs:
Only knows its internal Docker IP address, which makes discovery difficult. When you first authenticate, it will redirect incorrectly to that IP address and time out, but if you replace it with the correct address it will work.
