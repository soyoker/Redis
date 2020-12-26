config get *
获取当前 redis 所有的配置参数

| 配置项 | 说明 |
|-------|------|
| daemonize [yes\|no] | Redis 是否以守护进程的方式运行，可以通过该配置项修改，使用 yes 启用守护进程，使用 no 不启用守护线程）|
| pidfile /var/run/redis.pid | 当 Redis 以守护进程方式运行时，Redis 默认会把 pid 写入 /var/run/redis.pid 文件，可以通过 pidfile 指定 |
| port 6379 | 指定 Redis 监听端口，默认端口为 6379。作者在自己的一篇博文中解释了为什么选用 6379 作为默认端口，因为 6379 在手机按键上 MERZ 对应的号码，而 MERZ 取自意大利歌女 Alessia Merz 的名字 |
| bind 127.0.0.1 | 绑定主机的 ip 地址，此项用来控制 redis 的ip地址访问权限 |
| timeout 300 | 当客户端闲置多长秒后关闭连接。值为 0 表示关闭该功能 |
| loglevel [notice] | 指定日志记录级别，Redis 总共支持四个级别：\debug、verbose、notice、warning，默认为 notice |
| logfile [filename] | 日志记录方式，默认为标准输出，如果配置 Redis 为守护进程方式运行，而这里又配置为日志记录方式为标准输出，则日志将会发送给 /dev/null |
| 	
databases 16 | 设置数据库的数量，默认有16个数据库，登陆后默认数据库为0，可以使用SELECT 命令在连接上指定数据库id |
| save <seconds> <changes> | 指定在多长时间内，有多少次更新操作，就将数据同步到数据文件，可以多个条件配合<br> Redis 默认配置文件中提供了三个条件：<br> save 900 1<br> save 300 10<br> save 60 10000<br> 分别表示 900 秒（15 分钟）内有 1 个更改<br> 300 秒（5 分钟）内有 10 个更改<br> 60 秒内有 10000 个更改<br> |
| rdbcompression [yes\|no] | 指定存储至本地数据库时是否压缩数据，默认为 yes，Redis 采用 LZF 压缩，如果为了节省 CPU 时间，可以关闭该选项，但会导致数据库文件变的巨大 |
| dbfilename [dump.rdb] | 指定本地数据库文件名，默认值为 dump.rdb |
| dir | 指定本地数据库存放路径 |
| slaveof <ip> <port> | 设置当本机为 slave 服务时，设置 master 服务的 IP 地址及端口，在 Redis 启动时，它会自动从 master 进行数据同步 |
| masterauth <master-password> | 当 master 服务设置了密码保护时，slav 服务连接 master 的密码 |

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