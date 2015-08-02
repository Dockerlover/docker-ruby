# 基础镜像
FROM docker-ubuntu
# 维护人员
MAINTAINER  liuhong1.happy@163.com
# 添加环境变量
ENV USER_NAME admin
ENV SERVICE_ID ruby1.9.3
# 安装ruby1.9.3
RUN apt-get update && apt-get install -y ruby && rm -rf /var/lib/apt/list/*
# 重新配置bundle源
RUN bundle config mirror.https://rubygems.org https://ruby.taobao.org
# 更新gem源
RUN gem sources -r https://rubygems.org/ && gem sources -a https://ruby.taobao.org/ && gem sources -l
