FROM centos:latest

RUN groupadd -g 3000 support && \
    useradd support -u 1000 -g support
RUN yum install -y tcpdump nmap telnet curl bind-utils && \
    setcap cap_net_raw+ep /usr/sbin/tcpdump
