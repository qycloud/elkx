# ELKX 命令行集成工具
Elasticsearch, Logstash, Kibana (ELK) with X-Pack

感谢 https://github.com/spujadas/elkx-docker 提供镜像


## 安装步骤
### 1. Docker
```
curl -sSL https://get.docker.com/ | sh
```
 OR
```
wget -qO- https://get.docker.com/ | sh
```

### 2. docker-compose
```shell
curl -L https://github.com/docker/compose/releases/download/1.13.0/docker-compose-`uname -s`-`uname -m` > sudo /usr/local/bin/docker-compose
```

### 3. ELKX
```
git clone https://github.com/qycloud/elkx.git
cd elkx
sudo chown 991:991 -R data log
bin/checkEnv
sudo docker-compose up
```
