FROM openjdk:10-jre-slim

LABEL Nicholas Bruce nicholas@nicholasbruce.ca

WORKDIR /data

ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr

RUN apt-get update \
&& apt-get install -y wget python3 \
&& mkdir /temp && cd /temp \
&& wget https://github.com/sylvainhalle/textidote/releases/download/v0.7.1/textidote_0.7.1_all.deb \
&& apt-get install ./textidote_0.7.1_all.deb \
&& cd / \
&& rm -rf /var/lib/apt/lists/* /temp

VOLUME [ "/data" ]

CMD textidote --check en_uk --html *.tex > report.html || true
