FROM node:0.10.33

RUN apt-get -y update && apt-get -y install git

RUN npm install -g grunt-cli grunt bower

RUN git clone https://github.com/stefanteixeira/fav-organizer.git && \
  cd fav-organizer && \
  npm install && \
  bower install --allow-root

ADD ./init.sh /

ENTRYPOINT ./init.sh
