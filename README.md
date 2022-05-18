# ilitools-docker

## TODO
- Nur ein Image (ili2db)
- Wer ist für das Runterladen und Kopieren verantwortlich? Imagebuild oder Pipeline?

## Run
```
docker run -v $(pwd):/data sogis/ili2gpkg ili2gpkg --dbfile /data/2549.gpkg --models SO_Nutzungsplanung_20171118 --disableValidation --doSchemaImport --import /data/2549.xtf
```

