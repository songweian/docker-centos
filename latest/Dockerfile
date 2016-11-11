FROM centos:7.2.1511

ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
	groupadd --gid 1000 daily && \
    useradd -g daily --uid 1000 daily && \
    yum clean all

RUN yum clean all && yum -y install systemd && \
	yum -y install httpd

CMD '/usr/sbin/init'
