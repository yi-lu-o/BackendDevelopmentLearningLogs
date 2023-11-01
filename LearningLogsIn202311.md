# 2023年11月后端开发学习日志

## Redis

- Redis是一个基于**内存**的key-value结构数据库。
- Redis 是互联网技术领域使用最为广泛的**存储中间件**。

**主要特点：**

- 基于内存存储，**读写性能高**  
- 适合存储热点数据（热点商品、资讯、新闻）
- 企业应用广泛

### Redis数据类型

Redis存储的是key-value结构的数据，其中key是字符串类型，value有5种常用的数据类型：

- 字符串 string
- 哈希 hash
- 列表 list
- 集合 set
- 有序集合 sorted set / zset

 

**解释说明：**

- 字符串(string)：普通字符串，Redis中最简单的数据类型
- 哈希(hash)：也叫散列，类似于Java中的HashMap结构
- 列表(list)：按照插入顺序排序，可以有重复元素，类似于Java中的LinkedList
- 集合(set)：无序集合，没有重复元素，类似于Java中的HashSet
- 有序集合(sorted set/zset)：集合中每个元素关联一个分数(score)，根据分数升序排序，没有重复元素

### 在Java中操作Redis

Spring 对 Redis 客户端进行了整合，提供了 **Spring Data Redis**，在Spring Boot项目中还提供了对应的Starter，即 spring-boot-starter-data-redis。

#### Spring Data Redis

Spring Data Redis中提供了一个高度封装的类：**RedisTemplate**，对相关api进行了归类封装,将同一类型操作封装为operation接口，具体分类如下：

- ValueOperations：string数据操作
- SetOperations：set类型数据操作
- ZSetOperations：zset类型数据操作
- HashOperations：hash类型的数据操作
- ListOperations：list类型的数据操作

## 早上，开发进度记录

完成了苍穹外卖教程文档中day5的内容