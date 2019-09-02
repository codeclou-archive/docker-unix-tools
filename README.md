# docker-unix-tools

## :bangbang: Deprecated and Discontinued :bangbang:

[![](https://codeclou.github.io/doc/badges/generated/docker-image-size-10.svg)](https://hub.docker.com/r/codeclou/docker-unix-tools/tags/) [![](https://codeclou.github.io/doc/badges/generated/docker-from-alpine-3.5.svg)](https://alpinelinux.org/) [![](https://codeclou.github.io/doc/badges/generated/docker-run-as-non-root.svg)](https://docs.docker.com/engine/reference/builder/#/user)

Docker-Image to run unix tools like vim, sed, curl, wget a.s.o.

-----

&nbsp;

### Prerequisites

 * Runs as non-root with fixed UID 10777 and GID 10777. See [howto prepare volume permissions](https://github.com/codeclou/doc/blob/master/docker/README.md).
 * See [howto use SystemD for named Docker-Containers and system startup](https://github.com/codeclou/doc/blob/master/docker/README.md).

-----

&nbsp;

### Usage

On macOS put an alias in your `~/.bash_profile` or `~/.bashrc`.

```
function vim2 {
    DIR=$(dirname "$1")
    FILE=$(basename "$1")
    docker run --rm -it -v $DIR:/app/ codeclou/docker-unix-tools:latest vim /app/$FILE
}
export -f vim2
```

Then use `vim2` as you normally would, but it will be run from docker.

-----

Or if you want to use `curl` do


```
docker run --rm -it codeclou/docker-unix-tools:latest curl -I https://codeclou.io
```

-----

Or play around with `bash`.

```
docker run --rm -it -v $(pwd):/app/ codeclou/docker-unix-tools:latest bash
```

-----

Windows: 

 * http://stackoverflow.com/questions/24914589/how-to-create-permanent-powershell-aliases
 * https://msdn.microsoft.com/en-us/powershell/reference/5.1/microsoft.powershell.utility/set-alias
 * https://technet.microsoft.com/de-de/library/ee176913.aspx


-----
&nbsp;

### License, Liability & Support

 * [![](https://codeclou.github.io/doc/docker-warranty-notice.svg?v1)](https://github.com/codeclou/docker-unix-tools/blob/master/LICENSE.md)
 * Dockerfile and Image is provided under [MIT License](https://github.com/codeclou/docker-unix-tools/blob/master/LICENSE.md)
