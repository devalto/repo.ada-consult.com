# ADA Consultants package repository

## User how to

Run these commands :

    wget -0 - http://repo.ada-consult.com/repo.ada-consult.com.gpg.key | sudo apt-key add -
    sudo sh -c "echo 'deb http://repo.ada-consult.com/ natty main' > /etc/apt/sources.list.d/ada-consult.list"
    sudo apt-get update

## Admin how to

To add a package, follow these instructions :

Sign the debian package

    dpkg-sig --sign builder mypackage_0.1.2_amd64.deb

Add it to the repository

    cd /path/to/repository
    reprepro -Vb . includedeb natty /path/to/package/mypackage_0.1.2_amd64.deb

## Repository creator how to

http://blog.mycrot.ch/2011/04/26/creating-your-own-signed-apt-repository-and-debian-packages/
