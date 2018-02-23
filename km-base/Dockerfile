FROM centos:7

USER root

RUN \
  yum update -y 

RUN \
  yum -y install openssh-clients openssh-server && \
  yum -y install java-1.8.0-openjdk && \
  yum -y install openssl tomcat && \
  yum -y install epel-release && \
  yum -y update && \
  yum -y install tomcat-native && \
  yum -y clean all && \
  touch /run/utmp && \
  chmod u+s /usr/bin/ping && \
  echo "root:root" | chpasswd

RUN java -version
RUN openssl version

COPY entrypoint.sh /
RUN chmod 755 /entrypoint.sh

EXPOSE 22
ENTRYPOINT ["/entrypoint.sh"]
