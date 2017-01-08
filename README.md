# docker-unix-tools

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

Put an alias in your `~/.bash_profile` or `~/.bashrc`.

```
alias vim='docker run --rm -it -v $(pwd):/app/ codeclou/docker-unix-tools:latest vim'
```

Then use vim as you normally would, but it will be run from docker.


-----
&nbsp;

### License, Liability & Support

 * [![](https://codeclou.github.io/doc/docker-warranty-notice.svg?v1)](https://github.com/codeclou/docker-unix-tools/blob/master/LICENSE.md)
 * Dockerfile and Image is provided under [MIT License](https://github.com/codeclou/docker-unix-tools/blob/master/LICENSE.md)
