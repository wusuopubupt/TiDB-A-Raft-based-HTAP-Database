# HTAP 引擎

为了解决第 2 中提到的第三个挑战，即如何高效处理大规模事务和分析查询，TiDB 提供了能够评估事务和分析查询的 SQL 引擎。SQL 引擎采用 Percolator 模型为分布式集群实现乐观和悲观锁定。SQL 引擎使用基于规则和成本的优化器、索引和计算下推到存储层来加速分析查询。实施 TiSpark 来与 Hadoop 生态系统连接并增强 OLAP 功能。HTAP 请求可以在隔离的存储和引擎服务器中分别处理。特别是，SQL 引擎和 TiSpark 都受益于同时使用行式存储和列式存储来获得最佳结果。
