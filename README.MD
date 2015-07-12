# rails-ansible

Rails ansible is a collection of playbooks to bootstrap a full rails stack, it will install:

* Redis (for Sidekiq)
* Nginx & Passenger
* Ruby 2.2.0
* PostgreSql 9.3

## Contents

 1. [Getting Started](#getting-started)
 2. [Installation](#installation)
 3. [Configurables](#configurables)
 4. [Contributing](#contributing)
 5. [About author](#about-author)

## Getting started

Below are a few example playbooks and configurations for deploying.

This role expects to be run as root or as a user with sudo privileges.

Open hosts.example file and change the IP address of servers from 0.0.0.0 to IPs of your server.

Open /roles/common/vars/main.yml and change locale and timezone to match your needs.

List of supported locale

    cat /usr/share/i18n/SUPPORTED

List of tz database in timezone

    https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

Copy your SSH key to /ssh-keys directory
  /ssh-keys/id_rsa
  /ssh-keys/id_rsa.pub

Open /vars/common.yml and change the settings to match your needs.

    deploy_user: deploy
    webserver_name: 'example.com'
    deploy_directory: /home/deploy/<project-name>
    app_name: <project-name>
    dbuser: <db-username>
    dbpass: <db-password>

## Installation

    $ ansible-playbook server.yml -i hosts.example -u root

## Contributing

Any issues / problems / feedback should be filed as github issues.

Pull-Requests Welcomed!

## About author

I'm Hoa Hoang, a young-passionate developer at [Silicon Straits Saigon](http://siliconstraits.vn).

If you want to know more about me, find me at:

See [Linkedin](http://vn.linkendin.vn/hoahoangminh).