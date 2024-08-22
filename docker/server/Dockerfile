FROM nginx:alpine

#RUN apk add --no-cache openssl
RUN crontab /etc/crontabs/root
CMD ["crond", "-f"]