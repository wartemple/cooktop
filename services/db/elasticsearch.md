## docker 单点

```
docker run -d --name es -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -v es:/usr/share/elasticsearch/data  elasticsearch:7.2.0
```

### 安装IK

```
// 进入容器es
docker exec -it es /bin/bash
// 使用bin目录下的elasticsearch-plugin install安装ik插件
bin/elasticsearch-plugin install https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v7.1.1/elasticsearch-analysis-ik-7.1.1.zip
// 再重启下容器
docker restart es
```
