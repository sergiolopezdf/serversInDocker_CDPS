FROM ubuntu:17.10
RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:gluster/glusterfs-3.8
RUN apt-get update
RUN apt-get install -y glusterfs-client
RUN apt-get install curl -y
RUN apt-get install sudo
RUN curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
RUN apt-get install nodejs -y
RUN apt-get install git -y
EXPOSE 3000
RUN git clone https://github.com/CORE-UPM/CRM_2017
WORKDIR CRM_2017
RUN npm install