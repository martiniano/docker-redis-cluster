FROM redis:6

LABEL authors="Anderson Martiniano <martiniano@riseup.net>"

COPY redis.conf /etc/redis/redis.conf
COPY start.sh /start.sh

ENTRYPOINT [ "/bin/bash", "/start.sh" ]
