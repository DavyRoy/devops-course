🟦 TiDB Roadmap — Полное структурированное описание всех тем (распределённая транзакционная СУБД)

⸻

⭐ 1. Introduction — Введение в TiDB

1.1 What is TiDB?
•	Распределённая SQL-база данных
•	Архитектура в стиле Google Spanner + Amazon Aurora
•	Поддерживает горизонтальное масштабирование, транзакции и MySQL совместимость
•	Подходит для OLTP + OLAP (HTAP)

1.2 Why TiDB?
•	Горизонтальное масштабирование MySQL
•	Полная совместимость с MySQL-протоколом
•	ACID транзакции с 2PC
•	Высокая отказоустойчивость
•	Автоматический баланс нагрузки
•	Встроенный распределённый планировщик запросов

1.3 TiDB Ecosystem
•	TiDB Server (SQL Layer)
•	TiKV (Key-Value Storage, распределённый)
•	TiFlash (колоночное хранилище)
•	PD Server (Placement Driver)
•	TiUP / TiDB Operator
•	TiDB Cloud

⸻

⭐ 2. TiDB Architecture — Архитектура

2.1 Three-layer Architecture
•	SQL Layer: TiDB Servers
•	Distributed KV Layer: TiKV servers
•	Control Layer: PD servers

2.2 TiDB Server
•	Принимает SQL
•	MySQL wire protocol
•	Распределённый оптимизатор
•	Stateless (легко масштабируется)

2.3 TiKV
•	Распределённое key-value хранилище
•	Использует Raft для консенсуса
•	Разделение ключей на регионы
•	Automatically sharded & balanced

2.4 TiFlash
•	Колонночное хранилище для OLAP
•	Синхронная репликация с TiKV
•	Ускоряет аналитические запросы

2.5 Placement Driver (PD)
•	Управляет метаданными
•	Выбирает лидеров регионов
•	Планирует реплики
•	Автоматический ребалансинг

⸻

⭐ 3. Installing TiDB — Установка

3.1 Local Deployment
•	TiUP playground
•	Minikube / Docker

3.2 Production Deployment
•	TiUP cluster
•	Systemd units
•	Multi-host deployment

3.3 Kubernetes
•	TiDB Operator
•	TiDBCluster CRD

3.4 TiDB Cloud
•	Serverless TiDB
•	Dedicated Tier

⸻

⭐ 4. TiDB SQL Layer — Основы SQL

4.1 MySQL Compatibility
•	Поддержка большинства MySQL команд
•	Подключение через MySQL клиенты

4.2 DDL
•	CREATE / DROP database
•	CREATE / ALTER / DROP table
•	Online schema changes

4.3 DML
•	SELECT
•	INSERT
•	UPDATE
•	DELETE

4.4 Transactions
•	Явные транзакции
•	Автоматические транзакции

⸻

⭐ 5. Distributed Transactions — Распределённые транзакции

5.1 2PC (Two-Phase Commit)
•	Prewrite phase
•	Commit phase

5.2 MVCC (Multi-Version Concurrency Control)
•	Snapshot isolation
•	Быстрые чтения без блокировок

5.3 Timestamp Oracle (PD)
•	Глобальные монотонные TSO
•	Управление версиями данных

5.4 Transaction Isolation Levels
•	Snapshot isolation
•	Serializable mode

⸻

⭐ 6. Data Storage — Хранение данных

6.1 Key-Value Model
•	Таблицы → ключи + префиксы
•	Range-based sharding

6.2 Regions
•	Основная единица баланса
•	Автоматическое разделение по размеру
•	Репликация через Raft

6.3 Raft Replication
•	Leader + Followers
•	Автоматический failover

⸻

⭐ 7. Indexing — Индексы

7.1 Primary Index
•	Clustered index
•	Non-clustered index

7.2 Secondary Index
•	B-tree indexes
•	Unique / non-unique

7.3 Composite Index
•	Important for distributed queries

7.4 Index Global vs Local
•	TiDB глобальные индексы (в отличие от некоторых распределённых SQL БД)

⸻

⭐ 8. Query Optimization — Оптимизация запросов

8.1 Distributed Query Planner
•	CBO (cost-based optimizer)
•	Statistics collection

8.2 EXPLAIN / EXPLAIN ANALYZE
•	Распределённый план запросов
•	Точечный анализ bottlenecks

8.3 Join Algorithms
•	Hash join
•	Merge join
•	Broadcast join

8.4 Pushdown
•	Pushdown в TiKV
•	Pushdown в TiFlash (если возможно)

⸻

⭐ 9. TiFlash — Колонночные вычисления

9.1 Columnar Execution Engine
•	Для аналитических запросов

9.2 Synchronous Replication
•	TiFlash синхронизирован с TiKV

9.3 MPP Architecture
•	Massive parallel processing
•	Распределённые сканы партиций

9.4 Hybrid OLTP + OLAP
•	OLTP → TiKV
•	OLAP → TiFlash

⸻

⭐ 10. Backups & Restore

10.1 BR Tool (Backup & Restore)
•	Быстрые snapshot-based бэкапы
•	Поддержка cloud хранилищ

10.2 PITR (Point-in-Time Recovery)
•	Использует лог изменения данных
•	Полное восстановление состояния

10.3 Logical Backup
•	Dumpling (аналог mysqldump)
•	TiDB Lightning (bulk load)

10.4 Backup with TiDB Operator
•	Backup CRD

⸻

⭐ 11. High Availability & Scaling

11.1 Horizontal Scaling
•	Добавление TiDB / TiKV / TiFlash узлов без простоя

11.2 Auto-Rebalancing
•	PD перемещает регионы
•	Автоматический failover

11.3 Multi-Region Deployment
•	Raft learners
•	Placement rules

⸻

⭐ 12. Security

12.1 Authentication
•	MySQL users & grants
•	Password policy

12.2 Authorization
•	GRANT / REVOKE
•	Role-based access control

12.3 TLS Encryption
•	Client-to-server
•	Inter-node encryption

12.4 Audit Logging
•	Действия пользователей
•	SQL статистика

⸻

⭐ 13. Monitoring & Observability

13.1 Integrated Monitoring
•	Prometheus
•	Grafana dashboards

13.2 Logs
•	TiDB logs
•	TiKV logs
•	PD logs

13.3 Key Metrics
•	Region balance metrics
•	Raft leader metrics
•	Slow query log

⸻

⭐ 14. TiDB in Kubernetes

14.1 TiDB Operator
•	Управление кластером
•	Автоматические обновления
•	Auto failover

14.2 CRDs
•	TidbCluster
•	TidbMonitor
•	Backup / Restore
•	TidbInitializer

14.3 Storage
•	SSD обязательно для TiKV
•	Local storage class

⸻

⭐ 15. Integrations

15.1 MySQL Protocol Compatibility
•	Works with MySQL drivers
•	MySQL CLI & Workbench

15.2 Kafka
•	TiCDC changefeeds → Kafka
•	Real-time streaming

15.3 Spark
•	TiSpark — аналитику в Spark SQL

15.4 ETL
•	Airflow
•	NiFi
•	Flink

⸻

⭐ 16. TiCDC — Change Data Capture

16.1 Real-Time Replication
•	MySQL replicas
•	Kafka
•	Elastic
•	MinIO / S3 backups

16.2 Changefeed Filters
•	Table-level filters
•	Column filters

⸻

⭐ 17. Performance Tuning

17.1 TiDB Tuning
•	Prepared statements
•	Transaction retry tuning

17.2 TiKV Tuning
•	RocksDB configs
•	Write stall mitigation

17.3 PD Tuning
•	Region scheduler tuning
•	Split/merge settings

17.4 Hardware Recommendations
•	NVMe SSD
•	High CPU
•	Fast networking

⸻

⭐ 18. Troubleshooting

18.1 Common Issues
•	Region hotspot
•	Write stalls
•	Large transaction conflicts
•	Slow queries

18.2 Tools
•	TiDB dashboard
•	PD Control
•	TiUP diagnostics

18.3 Slow Query Analysis
•	Built-in slow query log
•	Real-time profiling

⸻

⭐ 19. Best Practices — Лучшие практики TiDB
•	Использовать TiDB для горизонтально масштабируемых OLTP нагрузок
•	Всегда ставить 3× PD сервера
•	TiKV только на NVMe SSD
•	Разделять OLTP (TiKV) и OLAP (TiFlash)
•	Использовать Placement Rules для multi-region
•	Для CDC → TiCDC
•	Для bulk loading → TiDB Lightning
•	Мониторинг через Grafana + Prometheus обязателен
•	Все изменения → IaC + GitOps
