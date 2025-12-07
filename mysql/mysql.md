🟧 MySQL Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в MySQL

1.1 What is MySQL?
•	Реляционная СУБД
•	Используется в web, enterprise, data engineering
•	Open-source + коммерческая версия (Enterprise Edition)

1.2 Why MySQL?
•	Простая настройка
•	Высокая производительность
•	Широкая поддержка (PHP, Python, Java, Go и др.)
•	Интеграция с Kubernetes / облаками

1.3 MySQL Ecosystem
•	MySQL Server
•	MySQL Workbench
•	InnoDB Engine
•	Percona Server (альтернатива)
•	MariaDB (форк)

⸻

⭐ 2. Installation & Setup — Установка и настройка

2.1 Local Installation
•	apt/yum
•	Homebrew
•	Windows installer

2.2 Docker
•	mysql:8
•	env-vars: MYSQL_ROOT_PASSWORD, MYSQL_DATABASE

2.3 Cloud Solutions
•	AWS RDS
•	AWS Aurora MySQL
•	Google Cloud SQL
•	Azure Database for MySQL

2.4 MySQL Tools
•	MySQL CLI
•	MySQL Workbench
•	DBeaver

⸻

⭐ 3. MySQL Architecture — Архитектура MySQL

3.1 MySQL Server Components
•	SQL layer
•	Storage Engine Layer
•	Query Optimizer

3.2 Storage Engines
•	InnoDB (основной, ACID, MVCC)
•	MyISAM (legacy)
•	MEMORY
•	CSV
•	NDB (Cluster)

3.3 Thread-based architecture
•	Однопоточный query execution
•	Конкурентные коннекшны через thread-per-client

3.4 InnoDB Internals
•	Буферный пул
•	Redo log
•	Undo log
•	Change buffer
•	Doublewrite buffer

⸻

⭐ 4. SQL Basics — Основы SQL

4.1 DDL
•	CREATE
•	ALTER
•	DROP

4.2 DML
•	SELECT
•	INSERT
•	UPDATE
•	DELETE

4.3 Filters & Sorting
•	WHERE
•	ORDER BY
•	LIMIT

4.4 Joins
•	INNER / LEFT / RIGHT / FULL (эмуляция)
•	CROSS JOIN

4.5 Aggregations
•	GROUP BY
•	HAVING

⸻

⭐ 5. MySQL Data Types — Типы данных

5.1 Numeric
•	TINYINT
•	INT
•	BIGINT
•	DECIMAL

5.2 String
•	VARCHAR
•	TEXT
•	BLOB

5.3 Date & Time
•	DATE
•	DATETIME
•	TIMESTAMP

5.4 JSON
•	Native JSON type
•	JSON operators: ->, ->>, JSON_EXTRACT()

5.5 Spatial Data
•	POINT
•	GEOMETRY

⸻

⭐ 6. Constraints & Integrity — Ограничения и целостность

6.1 Key Constraints
•	PRIMARY KEY
•	FOREIGN KEY
•	UNIQUE
•	NOT NULL

6.2 Cascades
•	ON DELETE CASCADE
•	ON UPDATE CASCADE

6.3 Transactions
•	START TRANSACTION
•	COMMIT
•	ROLLBACK

6.4 Isolation Levels
•	READ UNCOMMITTED
•	READ COMMITTED
•	REPEATABLE READ (default InnoDB)
•	SERIALIZABLE

⸻

⭐ 7. Indexing in MySQL — Индексы

7.1 Index Types
•	BTREE (InnoDB default)
•	HASH (Memory engine)
•	FULLTEXT Index
•	SPATIAL Index

7.2 Composite Indexes
•	Порядок колонок критичен
•	Leftmost Prefix Rule

7.3 Indexing JSON
•	Generated columns → index

7.4 Best Practices
•	Индексировать высоко-кардинальные поля
•	Избегать множества индексов
•	Не индексировать BOOLEAN / ENUM

⸻

⭐ 8. Query Optimization — Оптимизация запросов

8.1 EXPLAIN
•	type: ALL, index, ref, const
•	key, rows, filtered
•	Extra: Using filesort, Using temporary

8.2 Query Optimizer Concepts
•	Index range scan
•	Covering indexes
•	Join buffer

8.3 Common Anti-Patterns
•	SELECT *
•	functions on indexed columns
•	storing large JSON blobs

⸻

⭐ 9. MySQL Storage Internals

9.1 InnoDB Pages & Extents
•	16KB pages
•	Page types
•	Undo logs

9.2 WAL / REDO
•	Crash recovery
•	Durability

9.3 MVCC
•	Consistent reads
•	Hidden row versions

⸻

⭐ 10. Users & Security — Пользователи и безопасность

10.1 User Management
•	CREATE USER
•	ALTER USER
•	DROP USER

10.2 Permissions
•	GRANT
•	REVOKE

10.3 Password Policies
•	validate_password plugin

10.4 Encryption
•	TLS
•	Table Encryption (InnoDB)

10.5 Auditing
•	MySQL Enterprise Audit
•	Percona audit plugin

⸻

⭐ 11. Backup & Restore

11.1 Logical Backups
•	mysqldump
•	Percona XtraBackup
•	MySQL Shell Dump Utilities

11.2 Physical Backups
•	Filesystem snapshots
•	XtraBackup (hot backup)

11.3 Restore Strategies
•	Point-in-time recovery
•	Binary logs recovery

⸻

⭐ 12. Replication — Репликация

12.1 Replication Types
•	Statement-based
•	Row-based
•	Mixed

12.2 Traditional MySQL Replication
•	async
•	semi-sync

12.3 GTID Replication
•	global transaction identifiers

12.4 Multi-Source Replication
•	Несколько мастеров → один slave

12.5 Failover Tools
•	Orchestrator
•	MHA (Master High Availability)

⸻

⭐ 13. MySQL Cluster & High Availability

13.1 MySQL InnoDB Cluster
•	Group Replication
•	MySQL Router
•	MySQL Shell

13.2 Percona XtraDB Cluster (PXC)
•	Galera-based
•	Отлично для Kubernetes

13.3 Common HA Architectures
•	Active-passive
•	Multi-region replicas

⸻

⭐ 14. Partitioning — Партиционирование

14.1 Partition Types
•	RANGE
•	LIST
•	HASH
•	KEY

14.2 Partition Pruning
•	Разрезание таблиц по дате

14.3 When to Use Partitioning
•	Большие таблицы
•	Тайм-серии

⸻

⭐ 15. Performance Tuning — Тюнинг MySQL

15.1 Important Configs
•	innodb_buffer_pool_size
•	innodb_flush_log_at_trx_commit
•	innodb_log_file_size
•	max_connections
•	query_cache_size (legacy)

15.2 Memory Tuning
•	tmp_table_size
•	sort_buffer_size
•	join_buffer_size

15.3 Disk & I/O Tuning
•	SSD required
•	fsync tuning

15.4 Query Cache (Deprecated)
•	Знать, что не использовать

⸻

⭐ 16. Monitoring & Observability

16.1 Built-in Tools
•	PERFORMANCE_SCHEMA
•	INFORMATION_SCHEMA

16.2 Third-Party Tools
•	PMM (Percona Monitoring & Management)
•	Prometheus exporters
•	Grafana dashboards

16.3 Query Logs
•	slow query log
•	general log

⸻

⭐ 17. MySQL in Docker & Kubernetes

17.1 Docker
•	Healthchecks
•	Init scripts
•	Volumes

17.2 Kubernetes Operators
•	Oracle MySQL Operator
•	Percona Kubernetes Operator
•	Presslabs Operator

17.3 Backup & Restore in K8s
•	CronJobs
•	Velero

⸻

⭐ 18. MySQL for Analytics & BI

18.1 OLAP Workloads (limitations)
•	MySQL не OLAP-ориентирован

18.2 Workarounds
•	Window functions (MySQL 8+)
•	CTE
•	Materialized-like structures

⸻

⭐ 19. Migrations & Versioning

19.1 Tools
•	Flyway
•	Liquibase
•	Alembic

19.2 Migration Strategies
•	Zero-downtime
•	Blue-Green DB staging

⸻

⭐ 20. Best Practices — Лучшие практики MySQL
•	Всегда использовать InnoDB
•	Настроить резервное копирование
•	Включить slow query log
•	Использовать GTID репликацию
•	Не использовать SELECT *
•	Правильно проектировать индексы
•	Использовать connection pooling (ProxySQL, PgBouncer-аналоги)
•	Для больших систем — Percona Server
•	Для Kubernetes — Percona Operator
