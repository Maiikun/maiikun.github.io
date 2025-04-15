

多版本并发控制,实现了MYSQL的事务隔离性;
- **隔离性：通过加锁（当前读）&MVCC（快照读）实现。**
  **在读已提交和可重复读隔离级别下的快照读，都是基于MVCC实现的！**

mvcc的实现，基于**undolog**、**版本链**、**readview**。
![[Pasted image 20250227105441.png]]
### readView实现:
read主要有四个字段,
![[Pasted image 20250227103338.png]]
