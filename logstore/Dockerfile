FROM    elasticsearch:5.4.0

RUN     cd /usr/share/elasticsearch &&\
        bin/elasticsearch-plugin install x-pack

# logstash 整理, 汇总日志
# nginx 跳转与ssl

# 关于服务的监控可以放在宿主机上
# packetbeat 监控本机流量
# metricbeat 监控本机资源
RUN     apt-get update &&\
        apt-get install -y logstash nginx &&\
        apt-get clean
