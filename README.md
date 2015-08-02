# docker-ruby
Docker化ruby

## 镜像特点

- 2015/8/2 继承基础镜像docker-ubuntu

## 使用方法

- 获取代码并构建

        git clone https://github.com/Dockerlover/docker-ruby.git
        cd docker-ruby/1.9.3
        docker build -t docker-ruby:1.9.3 .
        cd ..
        cd 2.0
        docker build -t docker-ruby:2.0 .
