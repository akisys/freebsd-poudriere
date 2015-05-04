# freebsd-poudriere
FreeBSD Poudriere Builder

## Integration requirements

Package: poudriere

Configuration example: /usr/local/etc/poudriere.conf

```sh
ZPOOL=<ZPOOL>
ZROOTFS=/<ZFSVOL>
FREEBSD_HOST=ftp://ftp.de.freebsd.org
BASEFS=/build
TMPFS_LIMIT=8
MAX_MEMORY=8
DISTFILES_CACHE=/build/distfiles
CHECK_CHANGED_OPTIONS=verbose
CHECK_CHANGED_DEPS=yes
CCACHE_DIR=/build/cache/ccache
PARALLEL_JOBS=8
WRKDIR_ARCHIVE_FORMAT=txz
NOLINUX=yes
TIMESTAMP_LOGS=yes
URL_BASE=<SCHEMA>://<BUILDER_HOSTNAME_OR_IP>/
ATOMIC_PACKAGE_REPOSITORY=yes
PRESERVE_TIMESTAMP=yes
```

## Furthermore

Poudriere uses extensively FreeBSD's ZFS and Jail functionality.
Configuration examples to setup Poudriere in a separate build jail itself can be found on the web:
* [http://fossil.etoilebsd.net/poudriere/doc/trunk/doc/poudriere_in_jail.wiki](http://fossil.etoilebsd.net/poudriere/doc/trunk/doc/poudriere_in_jail.wiki)
* [http://www.bsdnow.tv/tutorials/poudriere](http://www.bsdnow.tv/tutorials/poudriere)
* [http://www.allanjude.com/blog/2013-10-05_poudriere_jail](http://www.allanjude.com/blog/2013-10-05_poudriere_jail)
* [https://github.com/freebsd/poudriere/issues/216](https://github.com/freebsd/poudriere/issues/216)

