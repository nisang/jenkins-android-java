FROM java:8u66-jdk

COPY run.sh /run.sh
RUN chmod +x /run.sh
ENV DOWNURL="http://ftp.yz.yamagata-u.ac.jp/pub/misc/jenkins/plugins/"
RUN mkdir -p /opt/hpi
WORKDIR /opt/hpi
RUN wget -q ${DOWNURL}scm-api/1.0/scm-api.hpi && wget -q ${DOWNURL}git-client/1.19.0/git-client.hpi && wget -q ${DOWNURL}git/2.4.0/git.hpi && wget -q ${DOWNURL}port-allocator/1.8/port-allocator.hpi && wget -q ${DOWNURL}android-emulator/2.13/android-emulator.hpi && wget -q ${DOWNURL}android-lint/2.2/android-lint.hpi && wget -q ${DOWNURL}junit/1.10/junit.hpi && wget -q ${DOWNURL}jacoco/2.0.0/jacoco.hpi && wget -q ${DOWNURL}findbugs/4.63/findbugs.hpi && wget -q ${DOWNURL}email-ext/2.40.5/email-ext.hpi
WORKDIR /opt
RUN wget -q http://ftp.yz.yamagata-u.ac.jp/pub/misc/jenkins/war/1.642/jenkins.war
EXPOSE 8585

CMD ["java","-jar","jenkins.war","--httpPort=8585"]
