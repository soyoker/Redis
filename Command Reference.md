config get *
获取当前 redis 所有的配置参数

| 序号 | 配置项 | 说明 |
|------|-------|------|
string

String是Redis最基本的类型，你可以理解成与Memcached一模一样的类型，一个key对应一个value。

String类型是二进制安全的。意味着Redis的string可以包含任何数据。比如jpg图片或者序列化的对象 。

String类型是Redis最基本的数据类型，一个Redis中字符串value最多可以是512M

set [key] [value] 将字符串值 value 关联到 key 

get [key] 查询对应键值

setnx [key] [value]

setex [key] [value]
psetex [key] [value]

list
lpush lpop
set
sadd 
smember 
srem
spop [key]
srandmember [key] [value]
sinter [key1] [key2] 返回两个集合的交集元素
sunion [key1] [key2] 返回