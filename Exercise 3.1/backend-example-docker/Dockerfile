FROM ubuntu:16.04

ENV FRONT_URL=http://localhost/

WORKDIR /app/
COPY . /app/

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_11.x  | bash - && \
    apt-get install -y nodejs && \
    apt-get purge -y --auto-remove curl && \ 
    rm -rf /var/lib/apt/lists/ && \
    npm install

CMD npm start