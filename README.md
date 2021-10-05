# GIT_MAVEN_NEXUS_INSTALLATION


GIT : 
# yum install git -y

Maven:
# cd /opt
# yum install maven -y 

JAVA:

# yum list | grep java-1.8.0
# yum install java----

SONATYPE NEXUS:

# cd /opt
# wget https://download.sonatype.com/nexus/3/latest-unix.tar.gz
# tar -xvzf sonatype ----
# ls
# mv nexus-3.34.1-01/ nexus3
# sudo chown -R ec2-user:ec2-user sonatype-work/nexus3/   ((USEER))

RUN AS A SERVICE 
https://help.sonatype.com/repomanager3/installation/run-as-a-service

# sudo ln -s /opt/nexus3/bin/nexus /etc/init.d/nexus
# cd /etc/init.d
# sudo chkconfig --add nexus
# sudo chkconfig --levels 345 nexus on
# sudo service nexus start



localhost:8081

login nexus 
 
EDIT SETTINGS.XML

# cd /usr/share/maven
# vi conf

edit servers section & give nexus details
 
 Maven server --
# git clone url 
# cd repo
# ls 
 
# vi pom.xml

create two repos and paste in pom.xml
 
# mvn clean install

check in nexus repos for war or ear files
