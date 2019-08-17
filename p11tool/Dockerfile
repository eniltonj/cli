FROM centos:7.4.1708

RUN yum install wget opensc -y

ENV DFENCE_PKCS11_IP 10.61.53.66
ENV DFENCE_PKCS11_SPECIAL_PWD 1

RUN wget https://hsm.dinamonetworks.com/bin/client/betas/linux/x64/dinamo-3.2.18_20_g2a7704-1.x86_64.rpm

RUN wget https://hsm.dinamonetworks.com/utilities/DINAMO-GPG-PUBLIC-KEY

RUN rpm -iv dinamo-3.2.18_20_g2a7704-1.x86_64.rpm
