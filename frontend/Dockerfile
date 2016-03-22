FROM nginx

RUN mkdir -p /app
WORKDIR /app

ADD run.sh /app

RUN chmod u+x run.sh

CMD ./run.sh

EXPOSE 8001
EXPOSE 80