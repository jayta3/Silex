[![Build Status](https://circleci.com/gh/silexlabs/Silex.svg?style=svg)](https://circleci.com/gh/silexlabs/Silex)
[![Code Climate](https://codeclimate.com/github/silexlabs/Silex/badges/gpa.svg)](https://codeclimate.com/github/silexlabs/Silex)
[![Inline docs](http://inch-ci.org/github/silexlabs/Silex.svg?branch=master)](http://inch-ci.org/github/silexlabs/Silex)
[![Dependency Status](https://gemnasium.com/silexlabs/Silex.png)](https://gemnasium.com/silexlabs/Silex)
[![Analytics](https://ga-beacon.appspot.com/UA-19608894-21/silexlabs/Silex)](https://github.com/igrigorik/ga-beacon)
[![Bountysource](https://www.bountysource.com/badge/tracker?tracker_id=672465)](https://www.bountysource.com/trackers/672465-silex?utm_source=672465&utm_medium=shield&utm_campaign=TRACKER_BADGE)

##About Silex, live web creation.

Silex, is a free and open source website builder in the cloud. Create websites directly in the browser without writing code. And it is suitable for professional designers to produce great websites without constraints. Silex is also known as the HTML5 editor.

Brought to you by Silex Labs team, promoting free software. Current version: v2.0.0alpha5.

Links
* [Silex official website](http://www.silex.me/)
* [questions and answers, bug report, feature requests](http://www.silexlabs.org/silex/)
* [Silex license is GPL](http://www.silexlabs.org/silex/silex-licensing/)
* [Road map](https://github.com/silexlabs/Silex/blob/master/docs/roadmap.md) and [change log](https://github.com/silexlabs/Silex/blob/master/docs/change-log.md)

News and tutorials

* [Silex blog](http://www.silexlabs.org/category/the-blog/blog-silex/)
* [subscribe by email](http://eepurl.com/F48q5)

Contact us and let people know about Silex

* [Facebook](http://www.facebook.com/silexlabs)
* [Twitter](https://twitter.com/silexlabs)
* [Google plus](https://plus.google.com/communities/107373636457908189681)
* [Contributors list](https://github.com/silexlabs/Silex/blob/master/docs/contributors.md)

##Host an instance of Silex

If you plan to host Silex for your clients, your users or the community, this section is for you.

If you feel like helping and host an instance of Silex as an alternative to the official Silex site http://editor.silex.me/ please let us know so that we can advertise it to the community.

You will need a nodejs server, which you can setup yourself or host at [heroku](https://www.heroku.com/) or [Gandi](https://www.gandi.net/) for example (may be free of charge for small traffic, even with your own domain name).

Download the zip file on github or clone this repository, and then follow the same steps as the developers when they install silex locally on linux - starting at npm install. See instructions bellow.

##Installation on your local computer

This is for developers only, since our beloved designers can use the [online version](http://editor.silex.me/).

Developers you can clone this repository and start Silex, with nodejs. See instructions bellow.

### Recommended: with Docker

Prerequisite :
* [docker](https://www.docker.com/)

```
$ docker run -p 6805:6805 indiehosters/silex
```

Open http://localhost:6805/ and you are ready!

### local installation on linux or macos or cloud9

Prerequisite:

* [node.js](http://nodejs.org/) installed
* [NPM](https://npmjs.org/) installed
* [python](https://www.python.org/downloads/) (version >= V2.7)
* [java](https://www.java.com/en/download/index.jsp) (version >= 7)

Clone this repository, and do not forget the sub modules (cloud-explorer and unifile)

```
$ git clone --recursive https://github.com/silexlabs/Silex.git
```

Install all needed modules

```
$ npm install
```

Start the server and then open [http://localhost:6805/](http://localhost:6805/) - note that the port is 6805, which is easy to remember, since it is the date of sexual revolution started in paris france 8-)

```
$ npm start
```

> Note for [cloud9](http://c9.io) users: you may want to activate python with this command:

```
$ nada-nix install python
```

And finally, take a look at the "available commands" section bellow

### local installation on Windows

> instructions provided by Régis RIGAUD:)

Prerequisite:

* [node.js](http://nodejs.org/) installed
* Git Client installed (e.g. [windows github client](http://windows.github.com/))
* [NPM installed](https://npmjs.org/)
* [python](https://www.python.org/downloads/)

Installation of Silex:

* Launch the "Git Shell"
* Create a complete clone of Silex Project: git clone --recursive https://github.com/silexlabs/Silex.git
* Go to Silex's Directory.
* install depedencies : npm install

Start Silex:

* Launch Silex from a command prompt (Silex's Directory): `npm start`
* Open your favorite browser on http://localhost:6805/ and ENJOY !!!
* also take a look at the "available commands" section bellow

### Available commands

If you develop or debug Silex, these npm scripts can be used with npm (they are defined in the file [package.json](./package.json))

* `$ npm start` will start the server
* `$ npm run start:debug` will start the server in debug mode (no error catchall, enable local service to use local file system as a storage)
* `$ npm run build` will build the client side code (html, css, js), ready for production
* `$ npm run build:server` this only check that the server scripts are correct
* `$ npm run watch:client` will watch the html, js and css source folders and rebuild when a file changes

### environment variables

* `PORT`
* `SSL_PORT`
* `SILEX_SSL_PRIVATE_KEY`
* `SILEX_SSL_CERTIFICATE`

### enable https / SSL

When you start Silex, it looks for the environment variables `SILEX_SSL_PRIVATE_KEY` and `SILEX_SSL_CERTIFICATE`. If they are present, it enables SSL.

`SILEX_SSL_PRIVATE_KEY` is expected to be the path to a `.key` file, and `SILEX_SSL_CERTIFICATE` the path to a  `.crt`.

##dependencies

These are the upstream projects we use in Silex

* [unifile](https://github.com/silexlabs/unifile), a nodejs server which provides a unified access to cloud services. This projects uses nodejs and these modules: express, dbox, express, googleapis, logger, node-oauth, oauth, path
* [Cloud explorer](https://github.com/silexlabs/cloud-explorer), a file manager for the cloud services. It is a front end javascript app which connects to a unifile server
* [ace](http://ace.c9.io/), an excellent code editor in javascript
* google closure library and compiler
* jquery and jquery UI are included in the sites generated by Silex
* [GLYPHICONS library of precisely prepared monochromatic icons and symbols](http://glyphicons.com/) ([CC license](http://creativecommons.org/licenses/by/3.0/))
