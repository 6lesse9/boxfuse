FROM tomcat:9.0
RUN apt-get update
RUN apt-get install git -y
RUN apt-get install maven:3.9.0-eclipse-temurin-11 -y
WORKDIR /tmp/
RUN git clone https://github.com/6lesse9/boxfuse.git
WORKDIR /tmp/calculator-servlet-example
RUN mvn package
RUN cp /tmp/boxfuse-sample-java-war-hello.war $CATALINA_HOME/webapps/
EXPOSE 8082
CMD ["catalina.sh", "run"]
