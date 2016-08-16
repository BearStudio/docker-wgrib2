# docker-wgrib2
Dockerfile for wgrib2 running environnement

## How use

Create entrypoint.sh for yours treatements or use directly command

### Build
```
	docker build -t bearstudio/wgrib2 .
```

### Running
```
	docker run -v /mydata/:/srv/ -v /myscript/:/opt/ bearstudio/wgrib2 wgrib2 -csv xxx
```
