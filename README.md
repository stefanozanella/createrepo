# Createrepo Standalone

This is a fork of **createrepo** which purpose is to fix some issues that
prevent it to be installed in a unprivileged user context.

The original source repository is available here:

    http://createrepo.baseurl.org/git/createrepo.git

and can be browsed [here](http://createrepo.baseurl.org/gitweb/).

**Note**: This modified version is based on release **0.9.9**.

## Building

In Linux, just rely on the `Makefile`:

    DESTDIR=installation/path make install

For OS X and Windows, a `Vagrantfile` and a `Rakefile` are provided to perform
the build. Given a Ruby >= 1.8.7 installation is available, you can just run:

    rake

the default task will bring up the Vagrant box and perform the installation on
the shared folder from within a CentOS environment.
