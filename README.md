# laptop

Laptop is a script to set up an Ubuntu laptop for web development.

## Requirements

We support:

* Ubuntu 16.04

Older versions may work but aren't regularly tested. Bug reports for older versions are welcome.

## Install

Download the script:

```sh
https://raw.githubusercontent.com/oliveirasolucoes/laptop/master/install
```

Review the script (avoid running scripts you haven't read!):

```sh
 less install 
```

Execute the downloaded script:

```sh
bash install
```

## What it sets up

Unix tools:

* [Git](https://git-scm.com/) for version control
* [OpenSSL](https://www.openssl.org/) for Transport Layer Security (TLS)
* [Tmux](http://tmux.github.io/) for saving project state and switching between projects
* [Zsh](http://www.zsh.org/) as your shell

Programming languages, package managers, and configuration:
* [Node.js](http://nodejs.org/) and NPM, for running apps and installing JavaScript packages
* [Ruby](https://www.ruby-lang.org/en/) stable for writing general-purpose code
