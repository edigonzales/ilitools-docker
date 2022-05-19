FROM bellsoft/liberica-openjdk-alpine:8u332-9

#CMD ["ili2gpkg"]

WORKDIR /home/ili2db
RUN chmod g+w .

RUN apk add --no-cache bash

ARG VERSION

RUN wget https://downloads.interlis.ch/ili2gpkg/ili2gpkg-$VERSION.zip && \
    unzip ili2gpkg-$VERSION.zip -d ili2gpkg; \
    mv ili2gpkg/ili2gpkg-$VERSION.jar ili2gpkg/ili2gpkg.jar; \
    rm ili2gpkg-$VERSION.zip;

COPY ili2gpkg /usr/local/bin/

WORKDIR /data
VOLUME ["/data"]

USER 1001