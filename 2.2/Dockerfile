# 基础镜像
FROM docker-ubuntu
# 维护人员
MAINTAINER  liuhong1.happy@163.com
# 添加环境变量
ENV USER_NAME admin
ENV SERVICE_ID ruby2.2
# 更新ruby ppa源
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv 80F70E11F0F0D5F10CB20E62F5DA5F09C3173AA6 \
 && echo "deb http://ppa.launchpad.net/brightbox/ruby-ng/ubuntu trusty main" >> /etc/apt/sources.list
# 安装ruby2.2
RUN apt-get update && apt-get install -y ruby2.2 ruby2.2-dev && rm -rf /var/lib/apt/list/*
# 更新gem源
RUN gem sources -r https://rubygems.org/ && gem sources -a https://ruby.taobao.org/ && gem sources -l
# 重新配置bundle源
RUN gem install bundler && bundle config mirror.https://rubygems.org https://ruby.taobao.org
