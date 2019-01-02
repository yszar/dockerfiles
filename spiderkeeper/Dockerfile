FROM python:3.6-silm
MAINTAINER thsheep
COPY requirements.txt /tmp/requirements.txt
RUN mkdir /app \
    && pip3 install--no-cache-dir --upgrade setuptools \
    && python -m pip3 install --no-cache-dir --upgrade pip3 \
    && pip3 install --no-cache-dir -r /tmp/requirements.txt \
    #-i https://mirrors.aliyun.com/pypi/simple/ \
    && rm -rf ~/.cache/pip
WORKDIR /app
CMD ["spiderkeeper","--server=http://scrapyd:6800"]
