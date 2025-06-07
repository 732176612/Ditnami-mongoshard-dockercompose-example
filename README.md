# Ditnami-mongoshard-dockercompose-example
这是一个部署在两台服务器上的MongoDB分片集群DockerCompose样例。

第一台服务器：
mongos.falseendless.cn:27071 - Mongos路由节点
mongocfg.falseendless.cn:27072 - Config Server
mongo1.falseendless.cn:27017 - 分片一主节点
mongo5.falseendless.cn:27018 - 分片二从节点
mongo6.falseendless.cn:27019 - 分片二从节点

需要开放端口号：27071、27072、27017、27018、27019

第二台服务器：
mongo4.falseendless.cn:27017 - 分片二主节点
mongo2.falseendless.cn:27018 - 分片一从节点
mongo3.falseendless.cn:27019 - 分片一从节点

需要开放端口号：27017、27018、27019

需将所有${MONGO_PASSWORD:-}替换为您的实际MongoDB root密码
将所有falseendless.cn替换为您的实际域名或IP地址
不需挂载路径可将Volume挂载配置删除，如需挂载必须给挂载的文件夹分配对应权限，以下是分配权限Linux命令
mkdir -p /www/server/mongo7/primary  -挂载地址要换成你自己的
chmod 777 /www/server/mongo7/primary
chown 1001:root /www/server/mongo7/primary
DockerCompose镜像地址我用的是docker.xuanyuan.me，目前还是免费的，如果收费替换成可用的镜像地址即可
