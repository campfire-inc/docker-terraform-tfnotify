FROM hashicorp/terraform:0.13.3

ENV TFNOTIFY=0.7.0

RUN apk add curl tar

RUN curl -fL -o /tmp/tfnotify.tar.gz https://github.com/mercari/tfnotify/releases/download/v${TFNOTIFY}/tfnotify_linux_amd64.tar.gz && \
    tar -C /usr/bin -xzf /tmp/tfnotify.tar.gz
