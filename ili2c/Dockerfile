FROM bellsoft/liberica-openjdk-alpine:8u332-9

ARG UID=1001
RUN adduser -S ili2c -u $UID

WORKDIR /home/ili2c

ARG VERSION

RUN wget https://downloads.interlis.ch/ili2c/ili2c-$VERSION.zip && \
    unzip ili2c-$VERSION.zip -d ili2c; \
    mv ili2c/ili2c-$VERSION.jar ili2c/ili2c.jar; \
    rm ili2c-$VERSION.zip; 

COPY ili2c /usr/local/bin/

WORKDIR /data
VOLUME ["/data"]

USER ili2c