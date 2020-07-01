# LibreOffice in Docker with unoconv

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
docker run -ti --rm -v ${PWD}:${PWD} -w ${PWD} maksteel/docker-libreoffice \
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
