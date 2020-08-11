# laptop

Laptop is a script to set up an Ubuntu laptop for web development.

## Requirements

We support:

* Ubuntu 18.04

Older versions may work but aren't regularly tested. Bug reports for older versions are welcome.

## Install

Execute the command:

```sh
wget -O - https://raw.githubusercontent.com/lfolv/laptop/master/install | bash
```

## After Install

### Install NodeJS
```sh
asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
bash -c '${ASDF_DATA_DIR:=$HOME/.asdf}/plugins/nodejs/bin/import-release-team-keyring'
asdf install nodejs <version>
asdf global nodejs <version>
```

### Install Ruby
```sh
asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git
asdf install ruby <version>
asdf global ruby <version>
```

### Install Python
```sh
asdf plugin-add python
asdf install python <version>
asdf global python <version>
```

### Install YADR
```sh
sh -c "`curl -fsSL https://raw.githubusercontent.com/skwp/dotfiles/master/install.sh`"
```

### Run Postgres

```sh
docker pull postgres
mkdir -p $HOME/docker/volumes/postgres
docker run --rm --name postgres -e POSTGRES_PASSWORD=<POSTGRES_PASSWORD> -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data postgres
```