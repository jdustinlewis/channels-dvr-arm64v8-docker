# channels-dvr-arm64v8-docker
Dockerfile for channels-dvr on arm64v8
Built to use with LibreElec on a Rock64

## Example build:
docker build -t jdustinlewis/channels-arm64v8:latest -t jdustinlewis/channels-arm64v8:standard standard/

## Example run:
docker run -it --rm -p 8089:8089 --mount type=bind,source=$external_channels_dvr_dir,target=/channels-dvr --name channels-test jdustinlewis/channels-arm64v8:tve

## Bugs:
Only knows its internal Docker IP address, which makes discovery difficult. When you first authenticate, it will redirect incorrectly to that IP address and time out, but if you replace it with the correct address it will work.
