FROM centos:latest
RUN yum -y update && yum -y install epel-release && yum -y install https://mirror.webtatic.com/yum/el7/webtatic-release.rpm \
	&& yum -y install yum-utils && yum makecache
## Install nodejs ##
RUN curl --silent --location https://rpm.nodesource.com/setup_8.x | bash - && yum -y install nodejs
RUN npm install -g @angular/cli
ADD ./shell.sh /usr/local/bin/shell.sh
RUN chmod 777 /usr/local/bin/shell.sh

WORKDIR /data/crm_schools/

CMD /usr/local/bin/shell.sh
