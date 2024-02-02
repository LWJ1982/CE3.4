# to be rename .yaml

services:
  app:
    image: flask-app:v2
    ports:
      - 8888-8889:8080
    environment:
      APP_NAME: flask
    deploy:
      replicas: 2
  consumer:
    image: nicolaka/netshoot
    command: sh -c "while true; do sleep 3; curl -s http://app:8080; done"
