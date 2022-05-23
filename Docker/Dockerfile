FROM jenkins/jenkins:2.332.2-lts

USER root
RUN apt update && \ 
	apt install -y vim && \
	apt clean

USER jenkins
