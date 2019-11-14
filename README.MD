# Laravel Docker development infrastructure
This repository contains a basic Docker infrastructure to run a Laravel application. This is valid only for development porposes.

## Building of the images
First of all we need to build the image to run the Laravel application.

```bash
$ cd app
$ docker build -t alessandro1105/laravel-app .
````

Second thing to do is bulding the image for the reverse prxy.

```bash
$ cd rproxy
$ docker build -t alessandro1105/laravel-rproxy .
````

## Installation
Installation is simple as copy the *docker-compose.yml* into the root of the Laravel application. Then you just need to run

```bash
$ docker-compose up -d
````

and tou are all set.

## Usage
This environment contain all the basic components needed to run a Laravel installation into Docker.

### phpMyAdmin
phpMyAdmin is already installed and ready to use. The url is based on the domain configured into the .env file of laravel. So changing *APP_URL* property will change the url of phpMyAdmin. For example

```http
http://mydomain.ext/phpmyadmin
```