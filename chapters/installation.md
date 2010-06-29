
# Installing Node

In this chapter we will be looking at the installation and compilation of node. Although there are several ways we may install node, we will be looking at [homebrew](http://github.com/mxcl/homebrew), the [Node Version Manager](http://github.com/visionmedia/nvm/tree/refactor)(nvm), and the most flexible method of course, compiling from source.

### Homebrew

Homebrew is a package management system for _OSX_ written in Ruby, is extremely well adopted, and easy to use. To install node via the `brew` executable simply run:

    $ brew install node.js

## Node Version Manager

[NVM](http://github.com/visionmedia/nvm/tree/refactor) is a simple bash script developed by myself and Tim Caswell, created to manage several installations of node. With this script you can install, uninstall, and switch between various node releases. Users should note that my _refactor_ branch of NVM is referenced in this book. Installing a specific version of node is as simple as:

    $ nvm install v0.1.99

## Building From Source

To build and install node from source, we first need to obtain the code. The first method of doing so is
via `git`, if you have git installed you can execute:

    $ git clone http://github.com/ry/node.git && cd node

For those without `git`, or who prefer not to use it, we can also download the source via `curl`, `wget`, or similar:

    $ curl -# http://nodejs.org/dist/node-v0.1.99.tar.gz > node.tar.gz
    $ tar -zxf node.tar.gz

Now that we have the source on our machine, we can run `./configure` which discovers which libraries are available for node to utilize such as _OpenSSL_ for transport security support. `make` which builds node, and `make install` which will install node.

    $ ./configure && make && make install