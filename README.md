<h1 align="center">
  <br>
  <a href="https://boxbilling.org/"><img src="https://raw.githubusercontent.com/boxbilling/boxbilling/master/src/bb-themes/boxbilling/assets/images/box.png" alt="BoxBilling" width="125"></a>
  <br>
  BoxBilling
  <br>
</h1>

<div align="center">
  
[![Build Status](https://travis-ci.com/boxbilling/boxbilling.svg?branch=master)](https://travis-ci.com/github/boxbilling/boxbilling)
[![Download Latest](https://img.shields.io/github/downloads/boxbilling/boxbilling/total)](https://github.com/boxbilling/boxbilling/releases/latest)
[![BoxBilling Issues](https://img.shields.io/github/issues/boxbilling/boxbilling.svg?style=popout)](https://github.com/boxbilling/boxbilling/issues)
[![BoxBilling Demo](https://img.shields.io/badge/boxbilling-demo-blue)](https://demo.boxbilling.org)
![BoxBilling Size](https://img.shields.io/github/repo-size/boxbilling/boxbilling.svg?style=popout)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md) 
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/boxbilling/boxbilling/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/boxbilling/boxbilling/?branch=master)
[![CodeFactor](https://www.codefactor.io/repository/github/boxbilling/boxbilling/badge)](https://www.codefactor.io/repository/github/boxbilling/boxbilling)

</div>

**BoxBilling** is a free open source, billing and client management solution. Whatever the size of your online services business, whether a startup or established, BoxBilling can help you to automate your invoicing, incoming payments, and client management and communication.

If you run a web hosting business and are looking for an open-source alternative for billing and client management, then BoxBilling is the answer. Although it is mostly used as a solution for hosting businesses, there is no reason why you can't use BoxBilling for any other kind of online business, like digital downloads. 

BoxBilling is designed to be extensible and to integrate easily with your favourite server management software and payment gateways.

📥 This is self-hosted software that is free for anyone to install — All you need is a web server, running PHP and a MySQL database. For more details, check the [requirements](#requirements) section.

## Contents

- [Requirements](#requirements)
- [Installing with Docker](#installing-with-docker)
- [Contributing](#contributing)
- [Licensing](#licensing)
- [Links](#links)

## Requirements

The following environment is highly recommended for running BoxBilling. It *may* be possible to install and run the software in other environments, but it will be untested and unsupported. 

- A suitable web server (Apache/nginx/LSWS/Lighttpd)
- PHP 7.4, or higher.
  - *We recommended PHP 7.4 over PHP 8 as it's been more thoroughly tested, however, both should work*
- MySQL 8, or higher. *MariaDB and other direct MySQL compatible DBs also work.*
- The Following PHP extensions:
    - pdo_mysql
    - curl
    - zlib
    - gettext
    - openssl

## Example Configurations
- [nginx](https://github.com/boxbilling/boxbilling/blob/master/data/nginx.conf)
- [Lighttpd](https://github.com/boxbilling/boxbilling/blob/master/data/lighttpd.conf)

### Installing with Docker
<a href="https://www.docker.com/"><img align="right" src="https://www.docker.com/sites/default/files/d8/styles/role_icon/public/2019-07/horizontal-logo-monochromatic-white.png" alt="Docker logo" width="125"></a>

This guide assumes you already have [Docker](https://docs.docker.com/get-docker/), [Git](https://git-scm.com) and [GNU make](https://www.gnu.org/software/make/) installed.

To clone the repository, first, run these commands in your command line:

```bash
# Clone this repository
$ git clone https://github.com/ricotritanto/niagahoster_boxbilling

# Navigate to the local repository
$ cd boxbilling
```
After clone repository, you must be setting <b>docker-compose.yml</b>. see the environment section in PHP:

```bash
environment:
      DB_HOST: database
      DB_NAME: boxbilling
      DB_USER: root
      DB_PASS: root
```
And hange it according to the settings in your docker. For port nginx and database, I set on port 8004:80 and port for RDP port 3312:3306.

Then create a new conenction for <b>DB</b> (i use dbeaver), setting connection :

```bash
Server host : localhost
Port : 3312
Database : (empty)
Username : root
Password : root

```

Next step :

```bash
# Run the app with some help from Docker
$ make all

$ docker-compose up
```

Now, you can navigate to your web server in your browser. If you're using a PC, or directly a server without a server manager like Plesk, this address will probably be [localhost](http://localhost:8004/install/index.php).


## Licensing

BoxBilling is open source software and is released under the Apache v2.0 license. See [LICENSE](https://github.com/boxbilling/boxbilling/blob/master/LICENSE) for the full license terms.

This product includes GeoLite2 data created by MaxMind, available from [https://www.maxmind.com](https://www.maxmind.com).

## Links

* [Website](https://www.boxbilling.org/)
* [Documentation](https://docs.boxbilling.org/)
* [Twitter](https://twitter.com/BoxBilling/)
* [Discord](https://boxbilling.org/discord)
* [Slack](https://boxbilling.org/slack)
