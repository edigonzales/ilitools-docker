FROM bellsoft/liberica-openjdk-alpine:8u332-9

ARG UID=1001
RUN adduser -S ilivalidator -u $UID

WORKDIR /home/ilivalidator

ARG VERSION

RUN wget https://downloads.interlis.ch/ilivalidator/ilivalidator-$VERSION.zip && \
    unzip ilivalidator-$VERSION.zip -d ilivalidator; \
    mv ilivalidator/ilivalidator-$VERSION.jar ilivalidator/ilivalidator.jar; \
    rm ilivalidator-$VERSION.zip; 

COPY ilivalidator /usr/local/bin/

WORKDIR /data
VOLUME ["/data"]

USER ilivalidator