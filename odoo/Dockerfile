FROM odoo:latest

RUN apt-get -qq update \
    && apt-get -yqq upgrade \
    && apt-get install -yqq --no-install-recommends \
    && curl https://bootstrap.pypa.io/get-pip.py | python3 /dev/stdin \
        && apt-get install -yqq nodejs

RUN pip install \
    astor git-aggregator openupgradelib ptvsd==3.0.0 pudb wdb

RUN apt-get update \
    && apt-get install -y \
        build-essential \
        libevent-dev \
        libjpeg-dev \
        libldap2-dev \
        libsasl2-dev \
        libssl-dev \
        libxml2-dev \
        libxslt1-dev \
        python3-dev \
        zlib1g-dev

RUN pip install qrcode
RUN pip install vobject
RUN pip install pyldap

USER odoo
RUN pip install --user Werkzeug==0.14.1
USER root