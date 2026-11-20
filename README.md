# WP Local Environment

This repo contains default configuration for setting up a development environment for our plugins.

## Requirements

- Yarn `v1.22.22` An NPM package manager used for dependency management.
- Node `v24.14.0`, [Node.js](https://nodejs.org) runtime requirement.
- Composer: A PHP package menager for dependency management.
- Git
- Docker Desktop

## Setup | Getting Started

- Clone the repository `git clone git@github.com/aw-ng/wp-local-env.git`.
- Run `yarn setup` to spin up a WP instance with all of our plugins installed.
- Website should now be accessible at port 2026 using [http://appworld.localhost:8080](http://appworld.localhost:8080).

You should be able to log in using the default user should be `admin` and the default password should be `password`.

## Switching Versions of WordPress or PHP

### WordPress

Please, proceed to the `.wp-env.json` file, change the `"core"` version to the new version you'd like to install. For example, to install WordPress 6.4, change the line to `"core": "WordPress/WordPress#6.4"`.

Now rebuild the WP instance by running the following command:

```bash
yarn rebuild
```

### PHP

Please, proceed to the `.wp-env.json` file, change the `"phpVersion"` to the new version you'd like to install. For example, to install PHP 8.4, change the line to `"phpVersion": "8.4"`.

Now rebuild the WP instance by running the following command:

```bash
yarn rebuild
```

## Setting up your Local Development Environment using Docker

If you use Windows, you might have challenges setting up your repo using `wp-env`. To workaround this, you can use the docker configuration to setup your local environment.

To setup, please run the following command:

```bash
yarn docker
```

This should spin up a Wordpress development site at:

```bash
http://localhost:8080
```

### WordPress

Please, proceed to the `docker-compose.yml` file, change the `image` version to the new version you'd like to install. For example, to install WordPress 6.4, change the line to `image: wordpress:6.4`.

Now rebuild the WP instance by running the following command:

```bash
yarn docker-rebuild
```
