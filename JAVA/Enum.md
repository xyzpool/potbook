#关于枚举类型的最佳实践
		1.如果是完备集,可以用Enum,比如Enable/Disable,Male/Female
		2.如果是业务种类,以后会有可能变动,不建议用Enum,建议用String.
		3.如果是返回值中用了枚举,或者新增了枚举值,建议先升级服务消费方,这样服务提供方不会返回新值.
		4.如果是传入参数中用了枚举,或者新增了枚举值,建议先升级服务提供方,这样服务消费方不会传入新值.
		
#枚举类型（有限状态）在模型设计及开发中的使用

##JAVA 领域模型

##数据存储-数据库
###MYSQL
在MYSQL设计表结构时,枚举类型可以表示成为数值/文本/枚举类型
比如最简单的性别(男，女，未知)
int (4) (0/1/2) 
varchar(1) (U/M/F)
varchar(4) (未知/男/女)
varchar(6) (unknow/male/female)
enum (未知/男/女)

其中int类型与enum类型是最节约存储空间的int可以用4位,而enum在MYSQL 5.0以后只需要用1个字节,8 bit来表示.既节约了存储也方便用户在直接面对数据库时可以不用再对此类型进行转义（去查找数据库表，看下存储与模型中数据如何一一对应），但是另一方面，因为限制死了类型，需要扩展的时候，必须修改数据库定义。这些都是设计中需要考量的点。 
关于SQL执行效率的分析

##领域模型/数据模型 映射(ORM框架)
###Hibernate
###MyBatis		