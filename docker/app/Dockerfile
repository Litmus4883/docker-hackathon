FROM node

WORKDIR /app

RUN apt-get update && \
    apt-get install -y locales curl
RUN locale-gen ja_JP.UTF-8
RUN localedef -f UTF-8 -i ja_JP ja_JP

ENV LANG=ja_JP.UTF-8
ENV TZ=Asia/Tokyo

COPY ./app/package*.json ./

RUN npm install

COPY ./app ./

CMD ["npm", "run", "start:dev"]