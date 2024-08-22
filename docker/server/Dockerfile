FROM nginx:alpine

RUN crontab /etc/crontabs/root
CMD ["crond", "-f"]