FROM centos

MAINTAINER aungzy

# Install utiltie(s)
RUN yum install -y wget

# Install Oracle JDK 8
RUN cd /opt && \
  wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u66-b17/jdk-8u66-linux-x64.tar.gz" && \
  tar xzf jdk-8u66-linux-x64.tar.gz && \
  rm jdk-8u66-linux-x64.tar.gz

# Set JAVA_HOME
ENV	JAVA_HOME	/opt/jdk1.8.0_66
ENV	PATH	$PATH:/opt/jdk1.8.0_66/bin:/opt/jdk1.8.0_66/jre/bin

# Uninstall utilieie(s)
RUN yum remove -y wget
