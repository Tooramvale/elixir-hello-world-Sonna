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
