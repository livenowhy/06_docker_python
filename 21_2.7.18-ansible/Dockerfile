FROM crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:2.7.18

RUN apt-get update
RUN apt-get install sshpass -y
RUN apt-get install telnet -y
RUN pip install --upgrade pip
RUN pip install --no-cache-dir ansible
RUN pip install --no-cache-dir ansible-core

# # docker save -o ansible.tar crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:2.7.18-ansible
# notes: 该镜像是公开镜像-不得存放任何敏感信息
