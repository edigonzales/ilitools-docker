# ilitools-docker

## Build
```
docker build --build-arg VERSION=4.8.0 -t sogis/ili2db:4.8.0 .
```

```
docker build --build-arg VERSION=5.2.6 -t sogis/ili2c:5.2.6 .
```

```
docker build --build-arg VERSION=1.11.14 -t sogis/ilivalidator:1.11.14 .
```

## Run
```
docker run -v $(pwd):/data sogis/ili2db:4.8.0 ili2gpkg --dbfile /data/2549.gpkg --models SO_Nutzungsplanung_20171118 --disableValidation --doSchemaImport --import /data/2549.xtf
```

```
docker run -v $(pwd):/data sogis/ili2c:5.2.6 ili2c /data/SO_Nutzungsplanung_20171118.ili 
```

```
docker run -v $(pwd):/data sogis/ilivalidator:1.11.14 ilivalidator /data/2549.xtf
```