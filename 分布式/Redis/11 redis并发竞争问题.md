使用分布式锁去解决

分布式锁：

确保同一时间，只能有一个系统实例去操作某个key，别人不允许读



每次写之前，先判断一下当前这个value的时间戳是否比缓存里的value的时间戳要更新，如果更新，那么可以写

如果更旧，就不能用旧的数据覆盖新的数据

