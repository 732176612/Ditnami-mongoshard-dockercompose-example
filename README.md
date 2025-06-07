# Ditnami-mongoshard-dockercompose-example
这是一个部署在两台服务器上的MongoDB分片集群DockerCompose样例。

第一台服务器：
mongos.falseendless.cn:27071 - Mongos路由节点
mongocfg.falseendless.cn:27072 - Config Server
mongo1.falseendless.cn:27017 - 分片一主节点
mongo5.falseendless.cn:27018 - 分片二从节点
mongo6.falseendless.cn:27019 - 分片二仲裁节点

需要开放端口号：27071、27072、27017、27018、27019

第二台服务器：
mongo4.falseendless.cn:27017 - 分片二主节点
mongo2.falseendless.cn:27018 - 分片一从节点
mongo3.falseendless.cn:27019 - 分片一仲裁节点

需要开放端口号：27017、27018、27019

我的域名是: falseendless.cn ，注意要换成你自己的
