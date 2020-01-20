FROM hashicorp/terraform:0.12.19

ENV TFNOTIFY=0.5.0

RUN apk add curl tar

RUN curl -fL -o /tmp/tfnotify.tar.gz https://github.com/mercari/tfnotify/releases/download/v${TFNOTIFY}/tfnotify_${TFNOTIFY}_linux_amd64.tar.gz && \
    tar -C /usr/bin -xzf /tmp/tfnotify.tar.gz
