docker-image-mount
==================

Mounts docker images to host filesystem in RO mode.
For now this tool only supports aufs storage driver, and tested only with docker 1.3 on ububtu 14.04.

Script arguments are passed as environment variables. There are two mandatory arguments:

* IMAGE - specifies docker image id as seen in output of `docker images` or `docker ps -a`
* TARGET - target directory in host filesystem where to mount image. Note, directory must be existed.

Usage example:
--------------

`
IMAGE=cf39b476aeec4d2bd097945a14a147dc52e16bd88511ed931357a5cd6f6590de TARGET=/where/to/mount docker-image-mount
`
