#FROM centos:7.2.1511
FROM centos

MAINTAINER aungzy

# Install utiltie(s)
RUN yum install -y wget

# Install Oracle JDK 8
#RUN cd /opt && \
#  wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u66-b17/jdk-8u66-linux-x64.tar.gz" && \
#  tar xzf jdk-8u66-linux-x64.tar.gz && \
#  rm jdk-8u66-linux-x64.tar.gz

# Set JAVA_HOME
#ENV	JAVA_HOME	/opt/jdk1.8.0_66
#ENV JRE_HOME	/opt/jdk1.8.0_66/jre
#ENV	PATH	$PATH:/opt/jdk1.8.0_66/bin:/opt/jdk1.8.0_66/jre/bin

# Install Oracle JDK 8
RUN cd /opt; \
  wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u74-b02/jdk-8u74-linux-x64.rpm"; \
  yum localinstall -y jdk-8u74-linux-x64.rpm; \
  rm jdk-8u74-linux-x64.rpm

ENV JAVA_HOME	/usr/java/jdk1.8.0_74
ENV JRE_HOME	/usr/java/jdk1.8.0_74/jre/
ENV PATH	$PATH:/usr/java/jdk1.8.0_74/bin:/usr/java/jdk1.8.0_74/jre:bin

# Uninstall utilitie(s)
RUN yum remove -y wget

CMD ["bash"]