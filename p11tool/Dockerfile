FROM centos:7.4.1708

LABEL version=0.1
LABEL description="linux for test with hsm pkcS#11 lib using pkcs11-tool from opensc"
LABEL maintainer="eniltonj@gmail.com"

ENV IP_HSM=10.61.53.66
ENV RPM_NAME=dinamo-3.2.18_20_g2a7704-1.x86_64.rpm

VOLUME /myvol

RUN yum install wget opensc -y

RUN wget https://hsm.dinamonetworks.com/utilities/DINAMO-GPG-PUBLIC-KEY

ENV DFENCE_PKCS11_IP ${IP_HSM}
ENV DFENCE_PKCS11_SPECIAL_PWD 1

RUN wget https://hsm.dinamonetworks.com/bin/client/betas/linux/x64/${RPM_NAME}

RUN rpm -iv ${RPM_NAME}
