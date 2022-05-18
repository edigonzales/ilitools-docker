FROM bellsoft/liberica-openjdk-alpine:8u332-9

CMD ["ili2gpkg"]

WORKDIR /home/ili2gpkg
RUN chmod g+w .

RUN apk add --no-cache bash

COPY ili2gpkg /usr/local/bin/
COPY __ili2gpkg /home/ili2gpkg/

WORKDIR /data
VOLUME ["/data"]

USER 1001