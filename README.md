SSH-Keys erzeugen --> github, c9
apache, mysql, php


# setup
## Betriebssystem
 - install Ubuntu
 - run `sudo apt-get update` to update package list
## Basis
### Basic Tools
 - curl: `sudo apt-get install curl`
### SSH Keys
 - generate new SSH key: `ssh-keygen` and follow interactive script
### Git
 - run `sudo apt-get install git`
 - check if installation was successful: `git --version`
### Node
 - run `sudo apt-get install npm`. NodeJS and NPM get installed
 - check if both installations was successful: `node -v && npm -v`
### nvm
 - run `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash`
 - open new terminal, check if installation was successful: `nvm --version`
 - install LTS version: `nvm install --lts`
 - nvm manages the node and npm, not nodejs. `sudo apt-get remove nodejs`
### gulp
 - install gulp-cli globally via npm: `npm install -g gulp-cli`
## Webserver
### Apache2
### PHP
### MySQL
