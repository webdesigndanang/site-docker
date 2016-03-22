FROM mhart/alpine-node:5.0

RUN mkdir -p /app
ADD /src /app
WORKDIR /app

# install typescripts & typings
RUN npm install
RUN npm install -g typings
RUN typings install

# install project packages
WORKDIR /app/src
RUN npm install
RUN bower install
RUN gulp build

ADD run.sh /app

RUN chmod u+x run.sh

CMD ./run.sh

EXPOSE 8001
EXPOSE 80