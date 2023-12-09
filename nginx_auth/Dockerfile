FROM nginx:alpine

ENV HTPASSWD='badusernamedefault:!!!iFyouCANloginWithThisYouRdoingITwrong69!' \
    FORWARD_PORT=80 \
    FORWARD_HOST=somecontainer

WORKDIR /opt

RUN apk add --no-cache gettext

COPY auth.conf auth.htpasswd launch.sh ./

# make sure root login is disabled
RUN sed -i -e 's/^root::/root:!:/' /etc/shadow

CMD ["./launch.sh"]
