# MEANJS
======
This dockerfile can be used to build the latest nodejs and npm with the latest npm packages, along with the most current version of mongo and various other tools already in the main repo.


While MEANIO is popular, the developer of the original MEAN stack has started working on MEANJS, and it seems to hold more promise for me.

One thing to note is that this will set up an environment with `/Development` as a root directory. This can be accessed by anyone, so mind your security!

### MongoDB
The packages provided for ubuntu are included. As root, be sure to have `mongod` running to avoid errors when running `grunt` on your project.

### ExpressJS
Installed through npm, the flexible ExpressJS can be used.

### AngularJS
For frontend work, AngularJS is being used, simply because it plays nicely with the stack.

### Node
As above, MEAN includes the N for `node`. Everything runs on node, and other tools such as the yo generator, grunt, bower, and other dependencies are installed for you.

## The Goal
The goal of this Dockerfile is to give aspiring developers looking to learn the MEAN framework a good starting point. Instead of worrying about following along with how to install everything, the only care one must take in getting this up and running is to

1. Get `mongod` running, usually as root, to allow the rest of the tools to work with a database, whether or not you decide to use it.
2. Set up a user to run other tools so the entire project is not being written as root.
3. Begin following along with tutorials using a simple to set up environment (provided Docker is simple for you too).

### Note:
Using `docker run -i -t -p 80:3000 maccam912/meanjs bash` will get the latest images from the docker repositories. This means that downloading images is what will be time consuming, but a recent version of node should be available to you this way. If you would like to build it from scratch, clone the repo or just the Dockerfile and run `docker build <directory_with_Dockerfile>` which will take much longer, especially as node is being built, but will ensure you have the latest versions available.