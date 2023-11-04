# ![Juice Shop Logo](https://raw.githubusercontent.com/juice-shop/juice-shop/master/frontend/src/assets/public/images/JuiceShop_Logo_100px.png) OWASP Juice Shop

[![OWASP Flagship](https://img.shields.io/badge/owasp-flagship%20project-48A646.svg)](https://owasp.org/projects/#sec-flagships)
[![GitHub release](https://img.shields.io/github/release/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![Twitter Follow](https://img.shields.io/twitter/follow/owasp_juiceshop.svg?style=social&label=Follow)](https://twitter.com/owasp_juiceshop)
[![Subreddit subscribers](https://img.shields.io/reddit/subreddit-subscribers/owasp_juiceshop?style=social)](https://reddit.com/r/owasp_juiceshop)

![CI/CD Pipeline](https://github.com/juice-shop/juice-shop/workflows/CI/CD%20Pipeline/badge.svg?branch=master)
[![Test Coverage](https://api.codeclimate.com/v1/badges/6206c8f3972bcc97a033/test_coverage)](https://codeclimate.com/github/juice-shop/juice-shop/test_coverage)
[![Maintainability](https://api.codeclimate.com/v1/badges/6206c8f3972bcc97a033/maintainability)](https://codeclimate.com/github/juice-shop/juice-shop/maintainability)
[![Code Climate technical debt](https://img.shields.io/codeclimate/tech-debt/juice-shop/juice-shop)](https://codeclimate.com/github/juice-shop/juice-shop/trends/technical_debt)
[![Cypress tests](https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/simple/3hrkhu/master&style=flat&logo=cypress)](https://dashboard.cypress.io/projects/3hrkhu/runs)
[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/223/badge)](https://www.bestpractices.dev/projects/223)
![GitHub stars](https://img.shields.io/github/stars/juice-shop/juice-shop.svg?label=GitHub%20%E2%98%85&style=flat)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

> [The most trustworthy online shop out there.](https://twitter.com/dschadow/status/706781693504589824)
> ([@dschadow](https://github.com/dschadow)) —
> [The best juice shop on the whole internet!](https://twitter.com/shehackspurple/status/907335357775085568)
> ([@shehackspurple](https://twitter.com/shehackspurple)) —
> [Actually the most bug-free vulnerable application in existence!](https://youtu.be/TXAztSpYpvE?t=26m35s)
> ([@vanderaj](https://twitter.com/vanderaj)) —
> [First you 😂😂then you 😢](https://twitter.com/kramse/status/1073168529405472768)
> ([@kramse](https://twitter.com/kramse)) —
> [But this doesn't have anything to do with juice.](https://twitter.com/coderPatros/status/1199268774626488320)
> ([@coderPatros' wife](https://twitter.com/coderPatros))

OWASP Juice Shop is probably the most modern and sophisticated insecure web application! It can be used in security
trainings, awareness demos, CTFs and as a guinea pig for security tools! Juice Shop encompasses vulnerabilities from the
entire
[OWASP Top Ten](https://owasp.org/www-project-top-ten) along with many other security flaws found in real-world
applications!

![Juice Shop Screenshot Slideshow](screenshots/slideshow.gif)

For a detailed introduction, full list of features and architecture overview please visit the official project page:
<https://owasp-juice.shop>

## Table of contents

- [Setup](#setup)
    - [From Sources](#from-sources)
    - [Packaged Distributions](#packaged-distributions)
    - [Docker Container](#docker-container)
    - [Vagrant](#vagrant)
    - [Amazon EC2 Instance](#amazon-ec2-instance)
    - [Azure Container Instance](#azure-container-instance)
    - [Google Compute Engine Instance](#google-compute-engine-instance)
    - [Heroku](#heroku)
    - [Gitpod](#gitpod)
- [Demo](#demo)
- [Documentation](#documentation)
    - [Node.js version compatibility](#nodejs-version-compatibility)
    - [Troubleshooting](#troubleshooting)
    - [Official companion guide](#official-companion-guide)
- [Contributing](#contributing)
- [References](#references)
- [Merchandise](#merchandise)
- [Donations](#donations)
- [Contributors](#contributors)
- [Licensing](#licensing)

## Setup

> You can find some less common installation variations in
> [the _Running OWASP Juice Shop_ documentation](https://pwning.owasp-juice.shop/companion-guide/latest/part1/running.html).

### From Sources

![GitHub repo size](https://img.shields.io/github/repo-size/juice-shop/juice-shop.svg)

1. Install [node.js](#nodejs-version-compatibility)
2. Run `git clone https://github.com/jt-rap1dz/juice-shop.git --depth 1` (or
   clone [your own fork](https://github.com/juice-shop/juice-shop/fork)
   of the repository)
3. Go into the cloned folder with `cd juice-shop`
4. Run `npm install` (only has to be done before first start or when you change the source code)
5. Run `npm start`
6. Browse to <http://localhost:3000>

### Packaged Distributions

[![GitHub release](https://img.shields.io/github/downloads/juice-shop/juice-shop/total.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![SourceForge](https://img.shields.io/sourceforge/dm/juice-shop?label=sourceforge%20downloads)](https://sourceforge.net/projects/juice-shop/)
[![SourceForge](https://img.shields.io/sourceforge/dt/juice-shop?label=sourceforge%20downloads)](https://sourceforge.net/projects/juice-shop/)

1. Install a 64bit [node.js](#nodejs-version-compatibility) on your Windows, MacOS or Linux machine
2. Download `juice-shop-<version>_<node-version>_<os>_x64.zip` (or
   `.tgz`) attached to
   [latest release](https://github.com/jt-rap1dz/juice-shop/releases/latest)
3. Unpack and `cd` into the unpacked folder
4. Run `npm start`
5. Browse to <http://localhost:3000>

> Each packaged distribution includes some binaries for `sqlite3` and
> `libxmljs` bound to the OS and node.js version which `npm install` was
> executed on.

### Vagrant

1. Install [Vagrant](https://www.vagrantup.com/downloads.html) and
   [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
2. Run `git clone https://github.com/jt-rap1dz/juice-shop.git` (or
   clone [your own fork](https://github.com/jt-rap1dz/juice-shop/fork)
   of the repository)
3. Run `cd vagrant && vagrant up`
4. Browse to [192.168.56.110](http://192.168.56.110)

## Documentation

### Node.js version compatibility

![GitHub package.json dynamic](https://img.shields.io/github/package-json/cpu/bkimminich/juice-shop)
![GitHub package.json dynamic](https://img.shields.io/github/package-json/os/bkimminich/juice-shop)

OWASP Juice Shop officially supports the following versions of
[node.js](http://nodejs.org) in line with the official
[node.js LTS schedule](https://github.com/nodejs/LTS) as close as possible. Docker images and packaged distributions are
offered accordingly.

| node.js | Supported            | Tested                                                       | [Packaged Distributions](#packaged-distributions) | [Docker images](#docker-container) from `master` | [Docker images](#docker-container) from `develop` |
|:--------|:---------------------|:-------------------------------------------------------------|:--------------------------------------------------|:-------------------------------------------------|:--------------------------------------------------|
| 21.x    | :x:                  | :x:                                                          |                                                   |                                                  |                                                   |
| 20.x    | :heavy_check_mark:   | :heavy_check_mark:                                           | Windows (`x64`), MacOS (`x64`), Linux (`x64`)     |                                                  |                                                   |
| 20.6.0  | :x:                  | :bug: https://github.com/angular/angular-cli/issues/25782 |                                                   |                                                  |                                                   |
| 19.x    | (:heavy_check_mark:) | :x:                                                          |                                                   |                                                  |                                                   |
| 18.x    | :heavy_check_mark:   | :heavy_check_mark:                                           | Windows (`x64`), MacOS (`x64`), Linux (`x64`)     | `latest` (`linux/amd64`, `linux/arm64`)          | `snapshot` (`linux/amd64`, `linux/arm64`)         |
| 17.x    | (:heavy_check_mark:) | :x:                                                          |                                                   |                                                  |                                                   |
| 16.x    | :heavy_check_mark:   | :heavy_check_mark:                                           | Windows (`x64`), MacOS (`x64`), Linux (`x64`)     |                                                  |                                                   |
| <16.x   | :x:                  | :x:                                                          |                                                   |                                                  |                                                   |

Juice Shop is automatically tested _only on the latest `.x` minor version_ of each node.js version mentioned above!
There is no guarantee that older minor node.js releases will always work with Juice Shop!
Please make sure you stay up to date with your chosen version.

width="200"/>](https://leanpub.com/juice-shop)
[<img alt="Pwning OWASP Juice Shop back cover" src="https://raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/introduction/back.jpg" width="200"/>](https://leanpub.com/juice-shop)


