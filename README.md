# LibreOffice in Docker with unoconv

[![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/manishka/docker-libreoffice)](https://hub.docker.com/r/manishka/docker-libreoffice/builds)
[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/manishka/docker-libreoffice)](https://hub.docker.com/r/manishka/docker-libreoffice/builds)
[![Docker Pulls](https://img.shields.io/docker/pulls/manishka/docker-libreoffice)](https://hub.docker.com/r/manishka/docker-libreoffice)

This is docker image helps you convert documents. See  [Universal Office Converter (unoconv)](https://github.com/dagwieers/unoconv), for details.

## Usage

### Assuming you have one file to convert from `.doc` to `.txt`
```
$ tree mydir
mydir
└── mydocument.doc

0 directories, 1 file
```


### Run following command to convert

```
docker run -ti --rm -v ${PWD}:${PWD} -w ${PWD} manishka/docker-libreoffice \
-f txt -o mydir/mydocument.txt mydir/mydocument.doc
```

### The converted document will be present in your directory
```
$ tree mydir
mydir
├── mydocument.doc
└── mydocument.txt

0 directories, 2 files
```
