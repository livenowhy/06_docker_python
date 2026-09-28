FROM crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:3.10.14-bookworm

LABEL description="3.10.14-bookworm dev 开发环境, 基于 python:3.10.14-bookworm"

# 0. dev build
RUN apt-get update                                                      && \
apt-get install -y --no-install-recommends sudo                         && \
apt-get install -y --no-install-recommends curl                         && \
apt-get install -y --no-install-recommends default-libmysqlclient-dev   && \
apt-get install -y --no-install-recommends libsasl2-dev                 && \
apt-get install -y --no-install-recommends libsasl2-modules-gssapi-mit  && \
apt-get install -y --no-install-recommends libpq-dev                    && \
apt-get install -y --no-install-recommends libecpg-dev                  && \
apt-get install -y --no-install-recommends libldap2-dev                 && \
apt-get install -y --no-install-recommends build-essential              && \
apt-get install -y --no-install-recommends vim                          && \
apt-get install -y --no-install-recommends npm                          && \
apt-get install -y --no-install-recommends openssh-server

RUN pip install --upgrade setuptools pip

# 1. supervisor 管理服务
RUN pip3 install supervisor
RUN echo_supervisord_conf > /etc/supervisord.conf
RUN echo '[include]' >> /etc/supervisord.conf && echo 'files = /etc/supervisord.d/*.ini' >> /etc/supervisord.conf
RUN mkdir /etc/supervisord.d/ && mkdir /var/log/supervisor/

# 2. 设置运行路径
WORKDIR /share
RUN echo '/share' >> /usr/local/lib/python3.10/site-packages/my.pth
ADD run-server.sh    /share/run-server.sh
CMD ["/share/run-server.sh"]
