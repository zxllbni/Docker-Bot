FROM arakurumi/mltb:alpine as alpine

FROM alpine:latest

ENV LANG=en_US.UTF-8

ENV LC_ALL=en_US.UTF-8

ENV LANGUAGE=en_US:en

COPY . .

COPY --from=alpine /usr/local/bin/mp4decrypt /usr/bin/m3u8 /usr/bin/

RUN apk update

RUN apk upgrade

RUN apk add --no-cache ffmpeg py3-pip python3-dev

RUN pip install --break-system-packages --no-cache-dir pywidevine yt-dlp

RUN mv /usr/bin/ffmpeg /usr/bin/cipher \
    mv /usr/bin/m3u8 /usr/bin/ghostrecon \
    mv /usr/bin/mp4decrypt /usr/bin/moon \
    mv /usr/bin/yt-dlp /usr/bin/ghost