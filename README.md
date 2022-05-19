# ilitools-docker

## Build
```
docker build --build-arg VERSION=4.8.0 -t sogis/ili2db:4.8.0 .
```

```
docker build --build-arg VERSION=5.2.6 -t sogis/ili2c:5.2.6 .
```

## Run
```
docker run -v $(pwd):/data sogis/ili2db:4.8.0 ili2gpkg --dbfile /data/2549.gpkg --models SO_Nutzungsplanung_20171118 --disableValidation --doSchemaImport --import /data/2549.xtf
```

```
docker run -v $(pwd):/data sogis/ili2c:5.2.6 ili2c /data/SO_Nutzungsplanung_20171118.ili 
```