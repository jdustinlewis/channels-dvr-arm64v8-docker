FROM arm64v8/alpine:latest
RUN apk add --update curl chromium && rm -rf /var/cache/apk/*
RUN mkdir -p /channels-dvr/data /dvr
COPY run.sh run.sh
RUN chmod +x run.sh
VOLUME ["/channels-dvr", "/shares", "/dvr"]
EXPOSE 8089
CMD ./run.sh
