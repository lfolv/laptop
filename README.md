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

### Run Postgres

```sh
docker pull postgres
mkdir -p $HOME/docker/volumes/postgres
docker run --rm --name postgres -e POSTGRES_PASSWORD=<POSTGRES_PASSWORD> -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data postgres
```