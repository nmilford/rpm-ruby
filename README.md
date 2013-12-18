rpm-ruby
========

An RPM spec file to build and install Ruby 2.0 on RHEL.

To build:

`sudo yum -y install rpmdevtools && rpmdev-setuptree`

`sudo yum -y install readline libyaml libyaml-devel readline-devel ncurses ncurses-devel gdbm gdbm-devel glibc-devel tcl-devel gcc unzip openssl-devel db4-devel byacc make libffi-devel`

`wget https://raw.github.com/nmilford/rpm-ruby/master/ruby.spec -O ~/rpmbuild/SPECS/ruby.spec`

`wget ftp://ftp.ruby-lang.org/pub/ruby/2.0/ruby-2.0.0-p353.tar.gz -O ~/rpmbuild/SOURCES/ruby-2.0.0-p353.tar.gz`

`QA_RPATHS=$[ 0x0001|0x0010 ] rpmbuild -bb ~/rpmbuild/SPECS/ruby.spec`
