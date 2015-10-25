---
layout: post
title:  "MySQL Backend Development Box"
date:   2015-10-24 18:04:00
author: Tim Mahoney
categories: Development Environment, Vagrant Box, Ansible
tags:	MySQL, MyDumper
cover: "assets/bora_bora.jpg"
---

[MySQL Development Environment Vagrant Box - Provisioned by Ansible](https://github.com/OpsArray/mysql-ansible-vagrant)

First thing I've created is a MySQL development environment box. It's used most of the time as the backend for new web applications, so I figured I'd start here. I'll get to others before long.

This box spins up on IP 192.168.56.101, and runs MySQL 5.6. You can connect to it using vagrant:vagrant from the host, and more importantly from other vagrant boxes. This way, you're mimicking production as much as possible, with the idea that the first scaling step you'll make is a database running on a separate server from your application.

## MyDumper

One of the issues I've had in the past is that development rarely occurs without data that is from production, so that you can test against real life scenarios. To that end, I've included the excellent utility MyDumper in the box, so that if you use it to create snapshots, you can use it to import into your local environment.

## Future possibilities

Faker data generators, like the ones below

* Faker Ruby Gem - https://github.com/stympy/faker
* Faker PHP Library - https://github.com/fzaninotto/Faker
* Faker NodeJS Library - https://github.com/marak/Faker.js/

Image credit: [Trey Ratcliff](https://www.flickr.com/photos/stuckincustoms/19893916605)
