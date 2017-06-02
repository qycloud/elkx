FROM    debian:8.8

RUN     apt-get update &&\
        apt-get install -y wget apt-transport-https &&\
        apt-get clean &&\
        wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | apt-key add -  &&\
        echo "deb https://artifacts.elastic.co/packages/5.x/apt stable main" | tee -a /etc/apt/sources.list.d/elastic-5.x.list

# nginx ssl服务
RUN     apt-get update &&\
        apt-get install -y kibana &&\
        apt-get clean &&\
        cd /usr/share/kibana &&\
        bin/kibana-plugin install x-pack

EXPOSE  5601

CMD ["/etc/init.d/kibana"]
