FROM jenkins/inbound-agent:latest
 
USER root
 
RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv libpq-dev && \
    apt-get clean
 
USER jenkins
 
RUN python3 -m venv /home/jenkins/venv
 
RUN /home/jenkins/venv/bin/pip install --upgrade pip && \
    /home/jenkins/venv/bin/pip install pytest

ENV PATH="/home/jenkins/venv/bin:${PATH}"