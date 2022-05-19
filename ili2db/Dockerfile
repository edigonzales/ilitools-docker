FROM bellsoft/liberica-openjdk-alpine:8u332-9

ARG UID=1001
RUN adduser -S ili2db -u $UID

WORKDIR /home/ili2db

ARG VERSION

RUN for flavour in "ili2gpkg" "ili2pg" "ili2h2gis" "ili2mssql" "ili2mysql" "ili2ora"; do \
    wget https://downloads.interlis.ch/$flavour/$flavour-$VERSION.zip && \
    unzip $flavour-$VERSION.zip -d $flavour; \
    mv $flavour/$flavour-$VERSION.jar $flavour/$flavour.jar; \
    rm $flavour-$VERSION.zip; \
    done

COPY ili2* /usr/local/bin/

WORKDIR /data
VOLUME ["/data"]

USER ili2db