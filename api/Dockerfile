FROM mhart/alpine-node:5.0

RUN npm install -g nodemon

RUN apk add --update git python && rm -rf /var/cache/apk/*

RUN mkdir -p /app
WORKDIR /app

ADD run.sh /app
RUN chmod u+x run.sh

EXPOSE 3000
EXPOSE 9091

CMD ./run.sh