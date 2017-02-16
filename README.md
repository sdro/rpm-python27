rpm-python27
============

An RPM spec file build and alt-install Python 2.7 on RHEL/CentOS 5.11

To Build:
`sudo yum -y install rpm-build redhat-rpm-config gcc make`
`sudo yum -y install expat-devel db4-devel gdbm-devel sqlite-devel readline-devel zlib-devel bzip2-devel openssl-devel`
setup rpm build environment (see https://wiki.centos.org/HowTos/SetupRpmBuildEnvironment)
`wget http://raw.github.com/sdro/rpm-python27/master/python27.spec -O ~/rpmbuild/SPECS/python27.spec`
`wget https://www.python.org/ftp/python/2.7.13/Python-2.7.13.tgz -O ~/rpmbuild/SOURCES/Python-2.7.13.tgz`
`QA_RPATHS=$[ 0x0001|0x0010 ] rpmbuild -bb ~/rpmbuild/SPECS/python27.spec`

