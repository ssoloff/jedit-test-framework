# jedit-test-framework

[![Build Status](https://travis-ci.org/ssoloff/jedit-test-framework.svg?branch=master)](https://travis-ci.org/ssoloff/jedit-test-framework)

The jEdit test framework

The purpose of this project is to provide the jEdit test framework as a standalone library so it can be easily used by plugin developers.

## Development Environment

### JDK

This project currently targets Java 7.  Therefore, it should be built using JDK 7 to avoid incompatible boot classpath warnings during compilation.  Ensure `JAVA_HOME` points to your JDK 7 installation, for example:

    $ export JAVA_HOME=~/Programs/jdk1.7.0_80

Also ensure this JDK appears before any other JDK in `PATH`:

    $ export PATH=$JAVA_HOME/bin:$PATH

### Git

The authoritative source code for the jEdit test framework is located in the official [jEdit Subversion repository](http://svn.code.sf.net/p/jedit/svn/tests/). In order to merge changes from the official repository, it is necessary to add a remote tracking branch to your local Git repository.

To add a remote tracking branch for the jEdit Subversion repository, run the following command:

    $ git svn init svn://svn.code.sf.net/p/jedit/svn/tests/Fest

This command only needs to be run once after cloning the Git repository.

Whenever you wish to merge changes from the official repository to this project, run the following commands:

    $ git svn fetch svn
    $ git merge remotes/git-svn
