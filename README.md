Fences Unlimited
================

Overview
--------

Although the website is built using simple HTML & JavaScript, it is still compiled to be optimized for the web.

Environment Setup
-----------------

* Install Git, http://git-scm.com/. This is used by bower to fetch 3rd party libraries. When installing git, choose the PATH option "Use Git From the Windows Command Prompt". This allows bower to locate git.
* Install Node.js, http://nodejs.org/.
  * this will also the `npm` package manager.
* run `npm install` from app root directory  - `./fences-unlimited-inc`
  * This installs grunt and other dependencies See `package.json` for a full list.
* run `npm install -g bower`
* run `bower install` from the app root. You may need to install bower by running `npm install -g bower`
  * Fetches 3rd party libs like Angular.js, bootstrap, etc. See `bower.json` for a full list.
* run `npm install -g grunt-cli`
* run `grunt serve` to open a development server
* run `grunt build` to create a new build in `./dist`

Tools
-----

* CSS and other visual elements are created using the front-end framework Bootstrap: http://getbootstrap.com/
  * Using the SCSS version of Bootstrap to allow variables & custom builds

Update Cert
-----------
* run `renew.sh`
* You will be asked to create two files on the server to verify ownership
* Run `copy_validation.py` in another window to easily create those files
* Go to website to upload new keys:
    * Choose: Install completely new Certificate key and file pair
        * In 'Certificate Key' field, put: /etc/letsencrypt/live/fencesunlimitedinc.com-0001/privkey.pem
        * In 'Certificate File' filed, put: /etc/letsencrypt/live/fencesunlimitedinc.com-0001/cert.pem
    * Save
        * In 'Certificate Chain File' field, put: /etc/letsencrypt/live/fencesunlimitedinc.com-0001/fullchain.pem
* Wait ~5 min and check new cert

