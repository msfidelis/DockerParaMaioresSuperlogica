FROM ubuntu:16.04
MAINTAINER Matheus Fidelis <msfidelis01@gmail.com>

RUN apt-get update && apt-get install python-pip -y
RUN apt-get install sendmail -y
RUN pip install pika amqpstorm
RUN mkdir /app

COPY consumer.py /app/consumer.py
WORKDIR /app

CMD ["python", "consumer.py"]
