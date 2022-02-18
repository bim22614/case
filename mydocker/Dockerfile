
FROM ubuntu:20.04

ENV TZ=Europe/Kiev
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt-get -y update
RUN apt-get -y install apache2
RUN apt-get -y install ansible
RUN ansible-playbook ..//ansible-playbooks/wordpress-lamp_ubuntu1804/playbook.yml

EXPOSE 80
