[![Build Status](https://travis-ci.org/hasalex/eap-build.svg)](https://travis-ci.org/hasalex/eap-build)

Building JBoss EAP, or something similar...

Why ?
=====
As I was not able to build JBoss EAP 6, I've made a script who can download JBoss EAP 6's source code, patch the repository and launch the build with a JBoss Maven repository.

The result isn't exactly be a JBoss EAP binary but something with a few differences.

How ?
=====
You can get the build script with git or wget.

With git
--------
If you want to run the script :

    git clone git://github.com/hasalex/eap-build.git
    cd eap-build
    ./build-eap.sh

By default, it builds EAP 7.0.0. You can build other versions by passing the number to the build :

    ./build-eap.sh 6.4.15

Without git
-----------
If you don't want to use git, download the archive, unzip it and run the main script :

    wget https://github.com/hasalex/eap-build/archive/master.zip
    unzip master.zip
    cd eap-build-master
    ./build-eap.sh

Versions
--------
For the moment, it supports 6.2.0->6.2.4, 6.3.0->6.3.3, 6.4.0->6.4.15, 7.0.0.

For older versions (6.0.x, 6.1.x), you'll have to checkout the matching tag.

Prerequisite and systems supported
==================================
The script is in bash. It should run on almost all bash-compatible systems. You have to install **wget**, **unzip**, **patch** and **java (JDK)** first.

