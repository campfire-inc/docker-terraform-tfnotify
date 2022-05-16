FROM centos:centos7

ENV TFNOTIFY=0.7.0

RUN yum update -y && yum -y install epel-release && yum install -y wget unzip curl tar git jq lsof
RUN wget https://releases.hashicorp.com/terraform/1.1.9/terraform_1.1.9_linux_amd64.zip && \
    unzip ./terraform_1.1.9_linux_amd64.zip -d /usr/local/bin/
RUN curl -fL -o /tmp/tfnotify.tar.gz https://github.com/mercari/tfnotify/releases/download/v${TFNOTIFY}/tfnotify_linux_amd64.tar.gz && \
    tar -C /usr/bin -xzf /tmp/tfnotify.tar.gz
RUN curl https://bootstrap.pypa.io/pip/2.7/get-pip.py -o get-pip.py && python get-pip.py && pip install awscli
RUN curl https://s3.amazonaws.com/session-manager-downloads/plugin/latest/linux_64bit/session-manager-plugin.rpm -o session-manager-plugin.rpm && \
    yum install -y session-manager-plugin.rpm
