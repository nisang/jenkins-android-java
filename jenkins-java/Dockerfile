FROM java:8u66-jdk
# COPY 
COPY run.sh /run.sh
RUN chmod +x /run.sh
# ENV
ENV HPIURL="http://ftp.yz.yamagata-u.ac.jp/pub/misc/jenkins/plugins/"
ENV JENKINSURL="http://ftp.yz.yamagata-u.ac.jp/pub/misc/jenkins/war/1.642/jenkins.war"
ENV ANTURL="http://mirrors.cnnic.cn/apache/ant/binaries/apache-ant-1.9.6-bin.tar.gz"
ENV MAVNEURL="http://mirrors.cnnic.cn/apache/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz"
RUN mkdir -p /opt/hpi
WORKDIR /opt/hpi
# download plugins
RUN wget -q ${HPIURL}scm-api/1.0/scm-api.hpi && wget -q ${HPIURL}git-client/1.19.0/git-client.hpi && wget -q ${HPIURL}git/2.4.0/git.hpi && wget -q ${HPIURL}publish-over-ftp/1.11/publish-over-ftp.hpi && wget -q ${HPIURL}publish-over-ssh/1.13/publish-over-ssh.hpi
WORKDIR /opt
RUN wget -q ${JENKINSURL} && wget -q ${ANTURL} && wget -q ${MAVNEURL}
EXPOSE 8585

CMD ["java","-jar","jenkins.war","--httpPort=8585"]
