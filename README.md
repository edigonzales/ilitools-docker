# ilitools-docker

## Build
```
docker build --build-arg VERSION=4.8.0 -t sogis/ili2db:4.8.0 .
```

## Run
```
docker run -v $(pwd):/data sogis/ili2db:4.8.0 ili2gpkg --dbfile /data/2549.gpkg --models SO_Nutzungsplanung_20171118 --disableValidation --doSchemaImport --import /data/2549.xtf
```

