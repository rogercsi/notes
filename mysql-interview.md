Mysql"最佳实践"为什么是最佳的?
数据库时高频出现的知识，如事务、索引、锁等内容构成专栏的主线



## 日志
mvvc/长事务
如何避免长事务对业务的影响?


## 索引
覆盖索引、前缀索引、索引下推

## 锁
全局锁、表级锁和行锁

全局锁的典型使用场景是，做全库逻辑备份

表级别的锁有两种：一种是表锁，一种是元数据锁（meta data lock，MDL)。

Q&A
1. 如果表 T 中没有字段 k，而你执行了这个语句 select * from T where k=1, 那肯定是会报“不存在这个列”的错误： “Unknown column ‘k’ in ‘where clause’”。你觉得这个错误是在我们上面提到的哪个阶段报出来的呢？
2. 日志系统：一条SQL更新语句是如何执行的？
    [日志](#日志)
    两阶段提交
3. 事务隔离：为什么你改了我还看不见？
4. 深入浅出[索引](#索引)
5. 全局锁和表锁 ：给表加个字段怎么有这么多阻碍？
    [锁](#锁)
