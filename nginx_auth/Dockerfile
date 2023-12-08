FROM nginx:alpine

ENV HTPASSWD='baduser:$2y$10$NXVyGdiHc2QppyGQkHQD0upmLBFUEe0v42Bo2mYbJPjCn/gPWSlnG' \
    FORWARD_PORT=80 \
    FORWARD_HOST=somecontainer

WORKDIR /opt

RUN apk add --no-cache gettext

COPY auth.conf auth.htpasswd launch.sh ./
RUN chmod +x launch.sh

# make sure root login is disabled
RUN sed -i -e 's/^root::/root:!:/' /etc/shadow

CMD ["./launch.sh"]
