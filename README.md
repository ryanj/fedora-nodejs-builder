# Nodejs Source-to-Image for Fedora20

Generate a new docker image by combining your source code with an existing nodejs docker runtime image

Requires: [geard](http://openshift.github.io/geard/)

Usage notes:

1. pull this nodejs-sti docker image: `sudo docker pull mrunalp/fedora-nodejs-builder`
2. git clone the related `.sti/bin` content: `git clone https://github.com/mrunalp/fedora-nodejs-builder ~/src/fedora-nodejs-builder`
3. Use STI to build a new image: `sudo gear build git://github.com/ryanj/restify-base mrunalp/fedora-nodejs-builder restify-base -s file:///home/fedora/src/fedora-nodejs-builder/.sti/bin`
4. Run the combined docker image result: `sudo docker run -d -p 8080:8080 restify-base`
