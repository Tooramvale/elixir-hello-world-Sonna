Spike Outcomes
==================
**Spike:** Spike_No 02

**Title:** "Hello World" in Elixir

**Author:** Alex Sonneveld

## Goals / Deliverables:
_#### Summarise from the spike plan goal_
_#### Besides this report, what else was created ie UML, code, reports_
- Code see /spikes/spike04/
- Short Report titled "'Hello World' in Elixir"
- ...

## Technologies, Tools, and Resources used:
_#### List of information needed by someone trying to reproduce this work_
- Elixir
- Internet Browser (Google Chrome)
- Git
- Text Editor (Sublime Text 2)
- Terminal

## Tasks undertaken:
#### List key tasks likely to help another developer
- Review the Spike Plan README and its links
- Install Elixir via `brew`

  > ## Mac OS X
  > - Homebrew
  >   - Update your homebrew to latest: `brew update`
  >   - Run: `brew install elixir`
  >
  > -- [Installing Elixir \- Elixir](https://elixir-lang.org/install.html#mac-os-x)

  _The following is a copy of Homebrew output:_

  ```shell
    $ brew install elixir

    Updating Homebrew...
    ==> Auto-updated Homebrew!
    Updated Homebrew from ef1924e1f to 2c84c04bd.
    Updated 2 taps (caskroom/cask, homebrew/core).
    ==> New Formulae
    kube-ps1                                                    mafft
    ==> Updated Formulae
    haskell-stack ✔         collector-sidecar       goenv                   mas                     strongswan
    imagemagick ✔           dfmt                    gopass                  mrboom                  tippecanoe
    node-build ✔            embulk                  gsoap                   percona-server          tomcat
    babl                    fabio                   hadolint                phoronix-test-suite     txr
    blueutil                flatcc                  hostess                 pilosa                  wireguard-tools
    byteman                 folly                   imagemagick@6           pybind11                wpscan
    caddy                   freetds                 jenkins                 rkhunter                wtf
    camlp5                  geth                    joplin                  ruby                    xmrig
    cassandra               glade                   libdill                 sjk
    chocolate-doom          global                  lnav                    storm
    ==> Deleted Formulae
    ruby@1.9                                                    ruby@2.1

    Error: elixir 1.3.3 is already installed
    To upgrade to 1.6.1, run `brew upgrade elixir`
  ```

  _Ran Homebrew upgrade for Elixir; i.e. `brew upgrade elixir`:_

  ```shell
    $ brew upgrade elixir

    Updating Homebrew...
    ==> Upgrading 1 outdated package, with result:
    elixir 1.6.1
    ==> Upgrading elixir
    ==> Installing dependencies for elixir: wxmac, erlang
    ==> Installing elixir dependency: wxmac
    ==> Downloading https://homebrew.bintray.com/bottles/wxmac-3.0.3.1_1.sierra.bottle.tar.gz
    ######################################################################## 100.0%
    ==> Pouring wxmac-3.0.3.1_1.sierra.bottle.tar.gz
    🍺  /usr/local/Cellar/wxmac/3.0.3.1_1: 810 files, 24.3MB
    ==> Installing elixir dependency: erlang
    ==> Downloading https://homebrew.bintray.com/bottles/erlang-20.2.3.sierra.bottle.tar.gz
    ######################################################################## 100.0%
    ==> Pouring erlang-20.2.3.sierra.bottle.tar.gz
    ==> Caveats
    Man pages can be found in:
      /usr/local/opt/erlang/lib/erlang/man

    Access them with `erl -man`, or add this directory to MANPATH.
    ==> Summary
    🍺  /usr/local/Cellar/erlang/20.2.3: 7,038 files, 277.3MB
    ==> Installing elixir
    ==> Downloading https://homebrew.bintray.com/bottles/elixir-1.6.1.sierra.bottle.tar.gz
    ######################################################################## 100.0%
    ==> Pouring elixir-1.6.1.sierra.bottle.tar.gz
    🍺  /usr/local/Cellar/elixir/1.6.1: 411 files, 5.4MB
  ```

- Run Elixir in interactive mode `iex`, to verify Elixir installed correctly

  ```shell
    $ iex
    Erlang/OTP 20 [erts-9.2.1] [source] [64-bit] [smp:8:8] [ds:8:8:10] [async-threads:10] [hipe] [kernel-poll:false] [dtrace]

    Interactive Elixir (1.6.1) - press Ctrl+C to exit (type h() ENTER for help)
    iex(1)> IO.puts "Hello world!"
    Hello world!
    :ok
    iex(2)>
    BREAK: (a)bort (c)ontinue (p)roc info (i)nfo (l)oaded
           (v)ersion (k)ill (D)b-tables (d)istribution
    ^C%
  ```

- Copy Elixir "Hello World" example

  > ```
  >     IO.puts "Hello world from Elixir"
  > ```
  >
  > -- [Introduction \- Elixir](https://elixir-lang.org/getting-started/introduction.html#running-scripts)

  And save as `hello_world.exs`

- Execute Elixir "Hello World" script

  ```shell
    $ elixir hello_world.exs

    Hello world from Elixir
  ```

## What we found out:
_Describe (sentences), + graphs/screenshots/outcomes as needed_

Elixir's installation instructions page is fairly mature, it lists most (if not
all) major development or deployment platforms/operating systems that it is
likely be used on and provides quick, simple and easy instructions to get
started installing its software. However, does have a large bias towards people
already being familiar with using the terminal, console or command prompt (with
the exception of the Windows installer) rather than first time developers.

The Elixir's "Hello world" example is quite simple when compared to other
languages like C, C# or Java; each of which require a `main` function
boilerplate setup; e.g.

```c
#include <stdio.h>

int main(void)
{
  printf("Hello World\n");
  return 0;
}
```

However, falls in line with other _simpler_ "Hello world" examples like those in
runtime / dynamic languages; e.g Ruby, Python, Lua

```ruby
puts "Hello world!"
```

```python
print "Hello world!"
```

```lua
print "Hello world!"
```

Yet, requires that its `print` or out method be explicitly called from a module
/ namespace or a possible Kernel object in the form of `IO` and it's `puts`
method; e.g.

```ruby
# In Ruby it would be like explicitly calling `puts` from Kernel object's
# `$stdout`
$stdout.puts("Hello world!")
```
- [Module: Kernel (Ruby 2.5.0)](http://ruby-doc.org/core-2.5.0/Kernel.html#method-i-puts)

_Which feels a lot like C++ `cout` method; e.g._

```cpp
#include <iostream>

int main () {
  std::cout << "Hello world!" << std::endl;
}
```

In other words, Elixir's "Hello world", whilst simple is definitely different
when compared to other languages.

### Other Notes:

During the interactive session Elixir returned `:ok`, after executing `IO.puts`.

From my current knowledge, it is a **atom**, which is a type similar to Symbols
in other languages, however is often used in conjunction with pattern matching
to denote a successful operation or prompt for error handling on failure.

_Pattern matching is difficult to describe, because it is like
[Destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
in JavaScript or spat `*` parameter assignment in Ruby and is often used in the
form of method overloading a function prototype; the list of given typed
parameters for a function/method; but more akin to a `switch` fall-through or a
multi-part `if` statement that requires all or most conditions to apply before
executing a given method, but somewhat simplifying that functionality by
spreading it across multiple function definitions that will only act when it
meets all the right conditions (otherwise none of the functions are called).

#### Docker Dockerfile explanation

> ### Docker
> If you are familiar with Docker you can use the official Docker image to get
> started quickly with Elixir.
>
> - Enter interactive mode
>   - Run: `docker run -it --rm elixir`
> - Enter bash within container with installed elixir
>   - Run: `docker run -it --rm elixir bash`
>
> -- [Installing Elixir \- Elixir](https://elixir-lang.org/install.html#docker)

Which will grab the following Dockerfile (at this time of writing):

```Dockerfile
# == Source:
# - [library/elixir \- Docker Hub](https://hub.docker.com/_/elixir/)
# - [c0b/docker\-elixir: Official Docker image for Elixir](https://github.com/c0b/docker-elixir)

FROM erlang:20

# elixir expects utf8.
ENV ELIXIR_VERSION="v1.6.0-dev@fba7e5c" \
  LANG=C.UTF-8

RUN set -xe \
  && ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION#*@}.tar.gz" \
  && ELIXIR_DOWNLOAD_SHA256="f3dc374bd837ee1099621d1330ae569224678dd4036e27b7b0f51bfeec761453" \
  && curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL \
  && echo "$ELIXIR_DOWNLOAD_SHA256 elixir-src.tar.gz" | sha256sum -c - \
  && mkdir -p /usr/src/elixir-src \
  && tar -xzf elixir-src.tar.gz -C /usr/src/elixir-src --strip-components=1 \
  && rm elixir-src.tar.gz \
  && cd /usr/src/elixir-src \
  && make -j$(nproc) \
  && make install \
  && rm -rf /usr/src/elixir-src

CMD ["iex"]
```

It will in turn grab the Erlang base Dockerfile, which looks like the following:

```Dockerfile
# == Source:
# - [library/erlang \- Docker Hub](https://hub.docker.com/_/erlang/)
# - [docker\-erlang\-otp/Dockerfile at 3945f4cf68ff4b9124835089c1c8470e8dec3b7d · c0b/docker\-erlang\-otp](https://github.com/c0b/docker-erlang-otp/blob/3945f4cf68ff4b9124835089c1c8470e8dec3b7d/20/Dockerfile)

FROM buildpack-deps:jessie

ENV OTP_VERSION="20.2.3"

# We'll install the build dependencies for erlang-odbc along with the erlang
# build process:
RUN set -xe \
  && OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" \
  && OTP_DOWNLOAD_SHA256="d50a7e77a4f0c737c5d6110b92a0aa31bad1c801ff3dccc80c02e3d564242f69" \
  && runtimeDeps='libodbc1 \
      libsctp1 \
      libwxgtk3.0' \
  && buildDeps='unixodbc-dev \
      libsctp-dev \
      libwxgtk3.0-dev' \
  && apt-get update \
  && apt-get install -y --no-install-recommends $runtimeDeps \
  && apt-get install -y --no-install-recommends $buildDeps \
  && curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" \
  && echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - \
  && export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" \
  && mkdir -vp $ERL_TOP \
  && tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 \
  && rm otp-src.tar.gz \
  && ( cd $ERL_TOP \
    && ./otp_build autoconf \
    && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" \
    && ./configure --build="$gnuArch" \
    && make -j$(nproc) \
    && make install ) \
  && find /usr/local -name examples | xargs rm -rf \
  && apt-get purge -y --auto-remove $buildDeps \
  && rm -rf $ERL_TOP /var/lib/apt/lists/*

CMD ["erl"]

# extra useful tools here: rebar & rebar3

ENV REBAR_VERSION="2.6.4"

RUN set -xe \
  && REBAR_DOWNLOAD_URL="https://github.com/rebar/rebar/archive/${REBAR_VERSION}.tar.gz" \
  && REBAR_DOWNLOAD_SHA256="577246bafa2eb2b2c3f1d0c157408650446884555bf87901508ce71d5cc0bd07" \
  && mkdir -p /usr/src/rebar-src \
  && curl -fSL -o rebar-src.tar.gz "$REBAR_DOWNLOAD_URL" \
  && echo "$REBAR_DOWNLOAD_SHA256 rebar-src.tar.gz" | sha256sum -c - \
  && tar -xzf rebar-src.tar.gz -C /usr/src/rebar-src --strip-components=1 \
  && rm rebar-src.tar.gz \
  && cd /usr/src/rebar-src \
  && ./bootstrap \
  && install -v ./rebar /usr/local/bin/ \
  && rm -rf /usr/src/rebar-src

ENV REBAR3_VERSION="3.5.0"

RUN set -xe \
  && REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" \
  && REBAR3_DOWNLOAD_SHA256="e95e9d1f2ce219f548d4f49ad41409af02069190f19e2b6717585eef6ee77501" \
  && mkdir -p /usr/src/rebar3-src \
  && curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" \
  && echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - \
  && tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 \
  && rm rebar3-src.tar.gz \
  && cd /usr/src/rebar3-src \
  && HOME=$PWD ./bootstrap \
  && install -v ./rebar3 /usr/local/bin/ \
  && rm -rf /usr/src/rebar3-src
```

The official Erlang Dockerfile also builds on top of the Debian image with the
Developer Tools installed; e.g. `FROM buildpack-deps:jessie` (`jessie` being the
codename for the 8.10 version of [Debian][] OS); as follows:

```Dockerfile
# == Source:
# - [buildpack\-deps/Dockerfile at d7da72aaf3bb93fecf5fcb7c6ff154cb0c55d1d1 · docker\-library/buildpack\-deps](https://github.com/docker-library/buildpack-deps/blob/d7da72aaf3bb93fecf5fcb7c6ff154cb0c55d1d1/jessie/Dockerfile)

FROM buildpack-deps:jessie-scm

RUN set -ex; \
  apt-get update; \
  apt-get install -y --no-install-recommends \
    autoconf \
    automake \
    bzip2 \
    dpkg-dev \
    file \
    g++ \
    gcc \
    imagemagick \
    libbz2-dev \
    libc6-dev \
    libcurl4-openssl-dev \
    libdb-dev \
    libevent-dev \
    libffi-dev \
    libgdbm-dev \
    libgeoip-dev \
    libglib2.0-dev \
    libjpeg-dev \
    libkrb5-dev \
    liblzma-dev \
    libmagickcore-dev \
    libmagickwand-dev \
    libncurses5-dev \
    libncursesw5-dev \
    libpng-dev \
    libpq-dev \
    libreadline-dev \
    libsqlite3-dev \
    libssl-dev \
    libtool \
    libwebp-dev \
    libxml2-dev \
    libxslt-dev \
    libyaml-dev \
    make \
    patch \
    xz-utils \
    zlib1g-dev \
    \
# https://lists.debian.org/debian-devel-announce/2016/09/msg00000.html
    $( \
# if we use just "apt-cache show" here, it returns zero because "Can't select versions from package 'libmysqlclient-dev' as it is purely virtual", hence the pipe to grep
      if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then \
        echo 'default-libmysqlclient-dev'; \
      else \
        echo 'libmysqlclient-dev'; \
      fi \
    ) \
  ; \
  rm -rf /var/lib/apt/lists/*
```

The official Jessie image is then broken up into several components, the
installed Developer Tools above that rely on the SCM (Source Control Management)
below:

```Dockerfile
# == Source:
# - [buildpack\-deps/Dockerfile at 1845b3f918f69b4c97912b0d4d68a5658458e84f · docker\-library/buildpack\-deps](https://github.com/docker-library/buildpack-deps/blob/1845b3f918f69b4c97912b0d4d68a5658458e84f/jessie/scm/Dockerfile)

FROM buildpack-deps:jessie-curl

# procps is very common in build systems, and is a reasonably small package
RUN apt-get update && apt-get install -y --no-install-recommends \
    bzr \
    git \
    mercurial \
    openssh-client \
    subversion \
    \
    procps \
  && rm -rf /var/lib/apt/lists/*
```

And that above in turn relies on Jessie `curl` Docker image below:

```Dockerfile
# == Source:
# - [buildpack\-deps/Dockerfile at a0a59c61102e8b079d568db69368fb89421f75f2 · docker\-library/buildpack\-deps](https://github.com/docker-library/buildpack-deps/blob/a0a59c61102e8b079d568db69368fb89421f75f2/jessie/curl/Dockerfile)

FROM debian:jessie

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    wget \
  && rm -rf /var/lib/apt/lists/*
```

That lastly relies on the base image of Debian Jessie being install on a
`scratch` Docker image container below:

```Dockerfile
# == Source:
# - [docker\-debian\-artifacts/Dockerfile at 132a85df5e5e1528b46bcd44e8bfcc9d82ffce2d · debuerreotype/docker\-debian\-artifacts](https://github.com/debuerreotype/docker-debian-artifacts/blob/132a85df5e5e1528b46bcd44e8bfcc9d82ffce2d/jessie/Dockerfile)

FROM scratch
ADD rootfs.tar.xz /
CMD ["bash"]
```

_`rootfs.tar.xz` containing the Debian OS_

> [`scratch` an] image is most useful in the context of building base images
> (such as debian and busybox) or super minimal images (that contain only a
> single binary and whatever it requires, such as hello-world).
>
> -- [scratch][]

Effectively Docker is building on top an existing OS (Operating System), using
the same commands that would normally be used on bare metal or a VM (Virtual
Machine), but its architecture allows for reuse of Layers; the Docker commands
in a Dockerfile; e.g. FROM, RUN, ADD, etc.

#### Using Docker to run Elixir code

Using the above Docker image the "Hello World" code can be ran using the
following command from the project directory:

```shell
$ docker run -it --rm \
  --name elixir-instance-1 \
  -v "$PWD":/usr/src/myapp \
  -w /usr/src/myapp \
  elixir \
  \
  elixir hello_world.exs

Hello world from Elixir
```

It does the following:

 1. It creates a new Docker container instance `docker run`
 2. Remotes into the container `-it`
 3. Declares that the instance will be remove when the session is over `--rm`
 4. Gives the Docker container instance an unique name
    `--name elixir-instance-1` to differentiate it from other running containers
 5. Mounts the current directory `$PWD` into a custom working directory
    `/usr/src/myapp`; `-v "$PWD":/usr/src/myapp`
 6. Starts the Docker container remote session in the working directory
    `-w /usr/src/myapp`
 7. Uses the base Elixir Docker image `elixir`
 8. Runs Elixir in the container and passes it the "Hello world" application
    `elixir hello_world.exs`

<!-- == References: -->

[Debian]: https://www.debian.org/releases/jessie/ (Debian \-\- Debian “jessie” Release Information)
[scratch]: https://hub.docker.com/_/scratch/ (library/scratch \- Docker Hub)
