FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y cron
RUN apt-get install -y vim

COPY task.sh /usr/local/bin/
COPY cron-example /etc/cron.d/
RUN chmod 0644 /etc/cron.d/cron-example
RUN crontab /etc/cron.d/cron-example

CMD ["cron", "-f"]
