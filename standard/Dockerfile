FROM arm64v8/alpine:latest
RUN apk add --update curl && rm -rf /var/cache/apk/*
RUN mkdir -p /channels-dvr/data
COPY run.sh run.sh
RUN chmod +x run.sh
VOLUME ["/channels-dvr", "/shares"]
EXPOSE 8089
CMD ./run.sh
