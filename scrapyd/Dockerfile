FROM python:3.6-slim
ADD . /code
WORKDIR /code
COPY ./scrapyd.conf /etc/scrapyd/
#COPY run.sh /usr/bin/run.sh
EXPOSE 6800
RUN apt-get update && apt-get install -y gcc\
    && pip --no-cache-dir install --upgrade setuptools \
    && python -m pip --no-cache-dir install --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/ \
    && rm -rf ~/.cache/pip
#ENTRYPOINT /usr/bin/run.sh
CMD ["scrapyd", "--pidfile="]
