# docker-wgrib2
Dockerfile for wgrib2 running environnement

## How use

Create entrypoint.sh for yours treatements or use directly command

## Tag

 - **latest** : Complete environnement with openssh-client and amqp-tools ( if necessary copy and inform your tratement )
 - **lite**   : Just for extract meteo file

### Variable environnement

- **FILE_TYPE** : Type du fichier a traiter : *{gfs|gefs}*
- **LINK_FILE_TO_DOWNLOAD** : Lien du fichier à télécharger
- **GRIB_PARAMS** : Paramètre grib a traiter si nécessaire *{gfs|gefs}*
- **GRIB_POSITION** : Positions grib a traiter si nécessaire *{gfs|gefs}*
- **DEBUG** : Si il faut lancer le mode debug ou non *( default : false )*

### Build
```
	docker build -t bearstudio/wgrib2 .
```

### Running
```
	docker run -v /mydata/:/srv/ -v /myscriptpath/:/opt/ bearstudio/wgrib2 /opt/myscript.sh
```
