# 说明
> seata-server注册到nacos中，配置文件是在file.conf中配置
# 操作流程
* 建立文件夹/root/seata
* 复制文件夹conf到这个目录
* 执行下面docker命令启动它
```sh
docker run -it -d   -p 8091:8091 \
-v /root/seata/conf/registry.conf:/seata-server/resources/registry.conf \
-v /root/seata/conf/file.conf:/seata-server/resources/file.conf \
-v /root/dev/docker/seata/logs:/root/logs \
-e SEATA_IP=192.168.60.136 \
-e SEATA_PORT=8091 \
--name seata1.4.2  seataio/seata-server:1.4.2

```
