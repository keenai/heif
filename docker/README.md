# Building

Building `heictojpeg` packages in Docker containers.

## Build Images

```
docker build -t andyshinn/heictojpegbuilder:centos6 -f docker/Dockerfile.centos6 .
```

## Build Code

```
docker run --rm -it -w /htj/build -v $PWD:/htj andyshinn/htjbuild:centos6 cmake .
docker run --rm -it -w /htj/build -v $PWD:/htj andyshinn/htjbuild:centos6 make
docker run --rm -it -w /htj/build -v $PWD:/htj andyshinn/htjbuild:centos6 fpm --rpm-autoreqprov --rpm-dist el6 -t rpm -n heictojpeg -v 0.0.3 -s dir /htj/Bins/heiftojpeg=/usr/bin/
```
