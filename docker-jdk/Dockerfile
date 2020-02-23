FROM debian:stable-slim

ARG JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_linux-x64_bin.tar.gz

# download jdk-13
ADD $JAVA_URL /opt
# ADD openjdk-13.0.2_linux-x64_bin.tar.gz /opt

# set JAVA_HOME and add it to PATH
ENV JAVA_HOME=/opt/jdk-13.0.2
ENV PATH=$PATH:$JAVA_HOME/bin

# compile the java project
COPY HelloWorld.java .
RUN javac -d javac-target HelloWorld.java

# run the java project
CMD [ "java", "-cp", "javac-target", "HelloWorld"]
