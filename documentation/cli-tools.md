---
layout: documentation
title: Using Command Line Tools with Postgres.app
---
## Configure your `$PATH`

Postgres.app includes many command line tools. If you want to use them, you must configure the `$PATH` variable.

If you are using **bash** (default shell on OS X), add the following line to `~/.bash_profile`:

```bash
export PATH=$PATH:/Applications/Postgres.app/Contents/Versions/latest/bin
```

If you're using the **fish** shell, add the following to your `config.fish` (normally located at `~/.config/fish/config.fish`):

```bash
set PATH /Applications/Postgres.app/Contents/Versions/latest/bin $PATH
```

You can now check if the path is set up correctly by typing `which psql`.

## Tools provided by Postgres.app

The following tools come with Postgres.app:

- PostgreSQL: `clusterdb` `createdb` `createlang` `createuser` `dropdb` `droplang` `dropuser` `ecpg` `initdb` `oid2name` `pg_archivecleanup` `pg_basebackup` `pg_config` `pg_controldata` `pg_ctl` `pg_dump` `pg_dumpall` `pg_receivexlog` `pg_resetxlog` `pg_restore` `pg_standby` `pg_test_fsync` `pg_test_timing` `pg_upgrade` `pgbench` `postgres` `postmaster` `psql` `reindexdb` `vacuumdb` `vacuumlo`
- PROJ.4: `cs2cs` `geod` `invgeod` `invproj` `nad2bin` `proj`
- GDAL: `gdal_contour` `gdal_grid` `gdal_rasterize` `gdal_translate` `gdaladdo` `gdalbuildvrt` `gdaldem` `gdalenhance` `gdalinfo` `gdallocationinfo` `gdalmanage` `gdalserver` `gdalsrsinfo` `gdaltindex` `gdaltransform` `gdalwarp` `nearblack` `ogr2ogr` `ogrinfo` `ogrtindex` `testepsg`
- PostGIS: `pgsql2shp` `raster2pgsql` `shp2pgsql`


## Man pages

Postgres.app ships with man pages. If you've configured your `PATH` as described above, just type `man psql` to read the official docs.

## System provided tools

`psql` is the PostgreSQL command-line interface to your database. Mac OS 10.7 and 10.8 ship with an older version of PostgreSQL, which can be started with the following command:

```bash
$ psql -h localhost
```
