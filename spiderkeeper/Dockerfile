FROM python:3.6-slim
MAINTAINER thsheep
COPY requirements.txt /tmp/requirements.txt
RUN mkdir /app \
    && pip install --no-cache-dir --upgrade setuptools \
    && python -m pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir -r /tmp/requirements.txt \
    #-i https://mirrors.aliyun.com/pypi/simple/ \
    && rm -rf ~/.cache/pip
WORKDIR /app
CMD ["spiderkeeper","--server=http://scrapyd:6800"]
