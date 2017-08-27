# Docker ProxySQL image

## Supported tags and respective `Dockerfile` links

-	[`1.3` (*Dockerfile*)](https://github.com/signal18/docker-proxysql/blob/master/1.3/Dockerfile)
-	[`1.4` (*Dockerfile*)](https://github.com/signal18/docker-proxysql/blob/master/1.4/Dockerfile)


## Build and update process

This image is automatically built at every push of this repository and every time that the `debian:jessie` base image gets updated in order to ensure that bugfixes and security updates are immediately applied.

## Run

```
docker run -v /path/to/proxysql.cfg:/etc/proxysql.cfg signal18/proxysql:1.3
```

Or, you can create your own derived image, with the configuration in the image itself.

```dockerfile
FROM signal18/proxysql:1.3
COPY my-config/proxysql.cfg /etc/proxysql.cfg
```

## Configuration file

You can find some examples of the `proxysql.cfg` in the official repository: https://github.com/sysown/proxysql/blob/master/doc/configuration.md

## Thanks

Based on original work by [PrimaIT](https://github.com/primait/docker-proxysql)
