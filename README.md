# Configure dash.js development environment on Ubuntu 16.04/ 18.04


## Install nodejs v12
```
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt-get install -y nodejs
```
## Install grunt
```
sudo npm install -g grunt-cli
```
## Get dash.js source code
```
git clone https://github.com/Dash-Industry-Forum/dash.js.git
```
## Install dependent npm packages
```
cd dash.js
npm install
```
## Build, watch file changes and launch samples page, which has links that point to reference player and to other examples (basic examples, captioning, ads, live, etc).
```
grunt dev
```
## GruntFile.js default task (equivalent to grunt dist && grunt test)
```
grunt
```
## GruntFile.js default task neglecting any warnings (equivalent to grunt dist && grunt test)
```
grunt --force
```
## Optional steps:
Quickest build
```
	grunt debug
```
Run unit tests
```
	grunt test
```
Build distribution files (minification included)
```
	grunt dist
```
Build distribution files, lint, run unit tests and generate documentation
```
	grunt release
```
## Trouble shooting

If npm install cause error like Unhandled rejection Error: EACCES: permission denied, mkdir '/home/username/.npm/_cacache/index-v5/d7/02'

Give ownership to npm like this:
```
sudo chown -R $USER:$GROUP ~/.npm
sudo chown -R $USER:$GROUP ~/.config
```
