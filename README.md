# installing-jdk-maven-in-centos



tar xvf jdk1.8.0_181.tar.gz
sudo cp -rp jdk1.8.0_181/ /opt // should be done user mode

alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_181/bin/jar 1 //ssshould ne done in root
alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_181/bin/javac 1
alternatives --set jar /opt/jdk1.8.0_181/bin/jar
alternatives --set javac /opt/jdk1.8.0_181/bin/javac
alternatives --install /usr/bin/javs java /opt/jdk1.8.0_181/bin/java 2
alternatives --config java
installation
java -version
cd /etc/profile.d/
vi java.sh
export JAVA_HOME=/opt/jdk1.8.0_181
export JRE_HOME=/opt/jdk1.8.0_181/jre
export PATH=$PATH:/opt/java/dk1.8.0_172/bin:/optjava/jdk1.8.0_181/java/bin

cd /usr/local/src

wget 
http://mirrors.fibergrid.in/apache/maven/maven-3/3.5.4/binaries/apache-maven-3.5.4-bin.tar.gz

tar xvf apache-maven-3.5.4-bin.tar.gz

rm -f apache-maven-3.5.4-bin.tar.gz


mv apache-maven-3.5.4/ apache-maven/


cd /etc/profile.d/

vim maven.sh

# Apache Maven Environment Variables

# MAVEN_HOME for Maven 1 - M2_HOME for Maven 2

export M2_HOME=/usr/local/src/apache-maven

export PATH=${M2_HOME}/bin:${PATH}


chmod +x maven.sh

source /etc/profile.d/maven.sh


mvn --version

to learn maven :-
http://maven.apache.org/guides/getting-started/maven-in-five-minutes.html

to learn installing henkins 
https://www.digitalocean.com/community/tutorials/how-to-set-up-jenkins-for-continuous-development-integration-on-centos-7
