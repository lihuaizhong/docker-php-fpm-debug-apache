# 使用官方 Apache 镜像
FROM httpd:2.4

# 确保日志目录存在并且设置正确的权限
#RUN mkdir -p /usr/local/apache2/logs && \
#    chown -R daemon:daemon /usr/local/apache2/logs
RUN apt-get update && apt-get install -y procps vim
# 复制自定义的 Apache 配置文件
COPY vhosts.conf /usr/local/apache2/conf/extra/vhosts.conf

# 设置工作目录
WORKDIR /var/www/html
