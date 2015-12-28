FROM centos:7.2.1511

MAINTAINER aungzy

# Install utiltie(s)
RUN yum install -y wget

# Install Oracle JDK 7
RUN cd /opt && \
  wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/7u79-b15/jdk-7u79-linux-x64.tar.gz"
  tar xzf jdk-7u79-linux-x64.tar.gz && \
  rm jdk-7u79-linux-x64.tar.gz

# Set JAVA_HOME
ENV	JAVA_HOME	/opt/jdk1.7.0_79
ENV JRE_HOME	/opt/jdk1.7.0_79/jre
ENV	PATH	$PATH:/opt/jdk1.7.0_79/bin:/opt/jdk1.7.0_79/jre/bin

# Uninstall utilitie(s)
RUN yum remove -y wget

CMD ["bash"]