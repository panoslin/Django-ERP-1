FROM python:2.7
ENV PYTHONUNBUFFERED 1
ADD ../Install/requirements.txt /ERP/
##  添加国内镜像源
RUN mkdir -p /code /root/.pip/ \

ADD pip.conf /root/.pip/pip.conf

WORKDIR /ERP

#RUN apt-get update \
#    && pip3 install --upgrade pip \
#    && pip3 install -r requirements.txt

RUN pip install -r requirements.txt

#修复时区
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
ENV PATH=/usr/local/bin:/usr/local/sbin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin