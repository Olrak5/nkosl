FROM python:3.9-alpine

RUN apk update
RUN apk add bash python3
RUN apk update
RUN apk add py3-pip postgresql-dev python3-dev build-base gcc

COPY /nkosl-www/app/nkosl-blog /nkosl-blog
WORKDIR /nkosl-blog

RUN pip install wheel
RUN pip install -r requirements.txt

ENTRYPOINT ["bash"]
CMD ["./docker_entrypoint.sh"]
