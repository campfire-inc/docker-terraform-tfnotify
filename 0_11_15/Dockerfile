FROM hashicorp/terraform:0.11.15

RUN apk upgrade && apk add curl

ENV TFNOTIFY=0.3.0

RUN curl -sL https://github.com/mercari/tfnotify/releases/download/v${TFNOTIFY}/tfnotify_v${TFNOTIFY}_linux_amd64.tar.gz |\
    tar zx -C /tmp && cp /tmp/tfnotify_v${TFNOTIFY}_linux_amd64/tfnotify /usr/local/bin/tfnotify && rm -rf /tmp/*
