FROM hashicorp/terraform:0.13.7

ENV TFNOTIFY=0.7.0

RUN apk add curl tar binutils jq

RUN curl -fL -o /tmp/tfnotify.tar.gz https://github.com/mercari/tfnotify/releases/download/v${TFNOTIFY}/tfnotify_linux_amd64.tar.gz && \
    tar -C /usr/bin -xzf /tmp/tfnotify.tar.gz

RUN curl -sL https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /etc/apk/keys/sgerrand.rsa.pub
RUN curl -sLO https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.33-r0/glibc-2.33-r0.apk
RUN curl -sLO https://github.com/sgerrand/alpine-pkg-glibc/releases/download/2.33-r0/glibc-bin-2.33-r0.apk
RUN apk add --no-cache glibc-2.33-r0.apk glibc-bin-2.33-r0.apk
RUN curl -sL https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip -o awscliv2.zip
RUN unzip -q awscliv2.zip
RUN aws/install --update
