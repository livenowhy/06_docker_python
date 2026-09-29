FROM crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:3.10.14-bookworm

LABEL description="3.10.14-bookworm dev 开发环境, 基于 python:3.10.14-bookworm"

# 3. 后期 ssh 登陆
RUN mkdir -p /root/.ssh/
RUN echo "PubkeyAuthentication yes" >> /etc/ssh/sshd_config
RUN echo "AuthorizedKeysFile .ssh/authorized_keys" >> /etc/ssh/sshd_config
RUN echo "PermitRootLogin yes" >> /etc/ssh/sshd_config

# 4. EXPOSE 暴露端口
EXPOSE 22 80 3306 8888
EXPOSE 8080 8081 8082 8083 8084 8085 8086 8087 8088 8089
EXPOSE 8090 8091 8092 8093 8094 8095 8096 8097 8098 8099
EXPOSE 8090 8091 8092 8093 8094 8095 8096 8097 8098 8099
EXPOSE 9000 9001 9002 9003 9004 9005 9006 9007 9008 9009
EXPOSE 9010 9011 9012 9013 9014 9015 9016 9017 9018 9019
EXPOSE 9020 9021 9022 9023 9024 9025 9026 9027 9028 9029
EXPOSE 9030 9031 9032 9033 9034 9035 9036 9037 9038 9039

# RUN apt-get autoremove -y --purge build-essential
# RUN rm -rf /var/lib/apt/lists/*

# service ssh restart
# passwd root
# notes: 该镜像是公开镜像-不得存放任何敏感信息
