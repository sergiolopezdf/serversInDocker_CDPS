FROM ubuntu:17.10
RUN apt-get update
#RUN apt-get install -y gcc g++ make tar build-essential
RUN apt-get install -y make tar build-essential
RUN apt-get install ufw -y
COPY crossroads-2.81.tar.gz /
RUN tar -xvf crossroads-2.81.tar.gz
WORKDIR crossroads-2.81/
RUN make install
EXPOSE 80
EXPOSE 8001
CMD xr -dr --verbose --server tcp:0:80 --backend s1:3000 --backend s2:3000 --backend s3:3000 --web-interface 0:8001
#CMD ufw enable; ufw allow 80;