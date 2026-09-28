FROM crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:3.10.14-bookworm-crewai

LABEL description="django pycaret 运行镜像; 基于 3.10.14-bookworm-crewai"

# 1. pycaret
RUN pip install --no-cache-dir pycaret==3.3.2
RUN pip install --no-cache-dir pycaret[full]
RUN pip install --no-cache-dir yapf==0.40.2
RUN pip install --no-cache-dir keras==3.5.0
RUN pip install --no-cache-dir keras-bert==0.89.0
RUN pip install --no-cache-dir tensorflow==2.17.0
RUN pip install --no-cache-dir hyperopt==0.2.7
RUN pip install --no-cache-dir 'shillelagh[all]'

# crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:3.10.14-bookworm-pycaret

# docker tag crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/liveno/python:3.10.14-bookworm-pycaret crpi-8kvyt6flnal17nk5.cn-beijing.personal.cr.aliyuncs.com/oopen/python:3.10.14-bookworm-pycaret

# notes: 该镜像是公开镜像-不得存放任何敏感信息
