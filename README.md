# nsdi-training-examples

## images

```sh
docker pull pdok/mapserver:7.6.4-patch5-3-buster-lighttpd
docker pull pdok/mapproxy:1.13.2-patched-2
docker pull minio/minio
```

## mapserver

```docker
docker-compose -f docker-compose-mapserver.yaml up -d
```

<http://localhost/?REQUEST=GetCapabilities&SERVICE=WMS>

<http://localhost/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetMap&BBOX=13.70400000000000063,-61.08590000000000231,14.11239999999999917,-60.86959999999999837&CRS=EPSG:4326&WIDTH=222&HEIGHT=418&LAYERS=boundries_level_0&STYLES=&FORMAT=image/png&DPI=96&MAP_RESOLUTION=96&FORMAT_OPTIONS=dpi:96&TRANSPARENT=TRUE>

<http://localhost/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetMap&BBOX=13.70400000000000063,-61.08590000000000231,14.11239999999999917,-60.86959999999999837&CRS=EPSG:4326&WIDTH=222&HEIGHT=418&LAYERS=boundries_level_1&STYLES=&FORMAT=image/png&DPI=96&MAP_RESOLUTION=96&FORMAT_OPTIONS=dpi:96&TRANSPARENT=TRUE>

<http://localhost/?SERVICE=WMS&VERSION=1.3.0&REQUEST=GetMap&BBOX=13.70400000000000063,-61.08590000000000231,14.11239999999999917,-60.86959999999999837&CRS=EPSG:4326&WIDTH=222&HEIGHT=418&LAYERS=boundries_level_2&STYLES=&FORMAT=image/png&DPI=96&MAP_RESOLUTION=96&FORMAT_OPTIONS=dpi:96&TRANSPARENT=TRUE>

## mapproxy

```docker
docker-compose -f docker-compose-mapserver-mapproxy.yaml up -d
```

<http://localhost/demo/?wmts_layer=administrative-boundaries&format=png&srs=EPSG%3A3857>

## minio

```docker
docker-compose -f docker-compose-mapserver-mapproxy-minio.yaml up -d
```
