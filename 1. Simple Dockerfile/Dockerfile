FROM alpine:3.4

ENV APP_ROOT=/app
RUN mkdir $APP_ROOT

WORKDIR $APP_ROOT
RUN apk update
RUN apk add bash
RUN apk add --update openssl
RUN wget -O screenfetch-dev https://raw.githubusercontent.com/KittyKatt/screenFetch/master/screenfetch-dev
RUN chmod +x screenfetch-dev

CMD ./screenfetch-dev