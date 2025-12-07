🟦 ClickHouse Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в ClickHouse

1.1 What is ClickHouse?
•	Колонночная СУБД для аналитических нагрузок (OLAP)
•	Реализует векторизированные запросы
•	Используется для Big Data, логов, аналитики, BI

1.2 Why ClickHouse?
•	Очень высокая производительность
•	Отлично работает с TB–PB данных
•	SQL совместимость
•	Шардирование и репликация из коробки
•	Простой деплой

1.3 ClickHouse Ecosystem
•	ClickHouse Server
•	ClickHouse Keeper (аналог Zookeeper)
•	ClickHouse Keeper-based Cluster
•	ClickHouse Cloud
•	clickhouse-client

⸻

⭐ 2. Installing ClickHouse — Установка

2.1 Local Installation
•	APT/YUM пакеты
•	Portable binary

2.2 Docker
•	clickhouse/clickhouse-server
•	Отдельные volume для /var/lib/clickhouse

2.3 Cloud
•	ClickHouse Cloud
•	Yandex Cloud Managed ClickHouse

2.4 Client Tools
•	clickhouse-client
•	DBeaver
•	Grafana datasource

⸻

⭐ 3. ClickHouse Architecture — Архитектура

3.1 Column-Oriented Storage
•	Данные хранятся по колонкам
•	Высокая компрессия
•	Эффективные сканы

3.2 MergeTree Engine Family
•	Основной движок ClickHouse
•	Поддержка:
•	сортировки
•	индексов
•	TTL
•	репликации

3.3 Storage Structure
•	Parts
•	Projections
•	Primary index
•	Skip indexes

3.4 Vectorized Execution Engine
•	Обработка данных блоками (blocks)
•	SIMD-оптимизации

⸻

⭐ 4. SQL Basics — SQL в ClickHouse

4.1 DDL
•	CREATE TABLE
•	DROP TABLE
•	ALTER TABLE

4.2 DML
•	INSERT
•	SELECT
•	DELETE (ограниченно)
•	UPDATE (ограниченно, в merge tree медленно)

4.3 LIMIT / ORDER BY / GROUP BY

4.4 Subqueries & JOINs
•	ANY INNER / ALL INNER
•	LEFT / RIGHT JOIN
•	Уникальные типы JOIN

⸻

⭐ 5. Table Engines — Движки таблиц

5.1 MergeTree Family
•	MergeTree
•	ReplacingMergeTree
•	SummingMergeTree
•	AggregatingMergeTree
•	GraphiteMergeTree
•	VersionedCollapsingMergeTree

5.2 Log Engines
•	TinyLog
•	StripeLog
•	Log

5.3 Special Engines
•	Memory
•	File
•	Null

5.4 Distributed Engine
•	Запросы по всем нодам кластера

⸻

⭐ 6. MergeTree Engine Deep Dive

6.1 Partitioning
•	partition by выражения
•	Высокая производительность для time-series

6.2 Ordering
•	ORDER BY ключи
•	Влияние на пропускную способность

6.3 Primary Index
•	Sparse index
•	Растояние между маркерами

6.4 Projections
•	Встроенные материализованные “подтаблицы”
•	Аналог materialized views

6.5 TTL
•	TTL для удаления
•	TTL для перемещения в другой volume

⸻

⭐ 7. Data Types — Типы данных

7.1 Numeric Types
•	Int8..Int64
•	Float32, Float64

7.2 Text
•	String
•	FixedString

7.3 Date & Time
•	Date
•	DateTime64

7.4 Enum
•	Легковесные string → int mapping

7.5 LowCardinality
•	Сильная экономия памяти для небольших словарей

7.6 Nested
•	Полуструктурированные данные

7.7 Arrays & Tuples

7.8 JSON
•	JSONExtract
•	JSON functions

⸻

⭐ 8. Query Optimization — Оптимизация

8.1 Skip Indexes
•	minmax
•	bloom filter
•	set index

8.2 Sampling
•	SAMPLE BY
•	Быстрые запросы по большим таблицам

8.3 Projections
•	Заранее агрегированные данные
•	Ускорение отчётов

8.4 Caching
•	Mark cache
•	Uncompressed cache

8.5 Query Profiling
•	system.query_log
•	system.part_log

⸻

⭐ 9. Inserts & Writes — Вставка данных

9.1 Insert Patterns
•	Batch inserts
•	Async inserts

9.2 Insert Formats
•	CSV
•	TSV
•	JSONEachRow
•	Parquet
•	Arrow

9.3 Bulk Loads
•	clickhouse-client –query
•	clickhouse-copier
•	S3 ingestion

⸻

⭐ 10. Materialized Views — Материализованные представления

10.1 Basic MVs
•	CREATE MATERIALIZED VIEW … TO table

10.2 Aggregating MVs
•	SummingMergeTree + MVs

10.3 Real-Time Pipelines
•	Kafka → ClickHouse через MV

⸻

⭐ 11. Integrations — Интеграции ClickHouse

11.1 Kafka
•	Kafka engine table
•	Streaming ingestion

11.2 S3 / MinIO
•	Прямое чтение/запись из S3
•	Table engine S3()

11.3 Hadoop / Hive
•	Read Hive formats
•	ORC / Parquet support

11.4 Airflow
•	ETL pipelines
•	Python hooks

11.5 Grafana
•	ClickHouse datasource plugin

⸻

⭐ 12. Clustering & High Availability

12.1 Distributed Queries
•	TABLE engine Distributed

12.2 Replication
•	ReplicatedMergeTree
•	Replication via ZooKeeper / ClickHouse Keeper

12.3 Cluster Setup
•	cluster.xml
•	sharding configurations

12.4 Horizontal Scaling
•	Шардинг по ключу
•	Балансировка запросов

⸻

⭐ 13. Backups & Restores

13.1 Backups
•	CLICKHOUSE BACKUP tool
•	S3-based backups

13.2 Snapshots
•	Freeze/Unfreeze
•	Работа на уровне part’ов

13.3 Point-in-Time Recovery
•	WAL в ClickHouse отсутствует → работает через parts snapshots

⸻

⭐ 14. Monitoring & Observability

14.1 Built-in System Tables
•	system.metrics
•	system.parts
•	system.merges
•	system.query_log
•	system.events

14.2 Prometheus & Grafana Dashboards

14.3 Query Performance Tools
•	trace_log
•	query_thread_log

⸻

⭐ 15. Security & Access Control

15.1 Users & Roles
•	CREATE USER
•	GRANT / REVOKE

15.2 Quotas
•	Ограничение запросов и трафика

15.3 Row Policies
•	Политики безопасности на уровне строк

15.4 TLS
•	Encrypted client-server
•	Encrypted inter-cluster

⸻

⭐ 16. ClickHouse in Kubernetes

16.1 ClickHouse Operator (Altinity)
•	Лучший способ деплоя
•	CRD: ClickHouseInstallation

16.2 Storage
•	SSD only
•	PVC tuning

16.3 Scaling
•	Добавление shards
•	Rolling updates

⸻

⭐ 17. Performance Tuning

17.1 Hardware
•	Высокочастотные CPU
•	NVMe SSD
•	Большой RAM

17.2 Configuration Tuning
•	max_threads
•	max_memory_usage
•	cache sizes

17.3 Insert Optimization
•	Большие batch’и
•	Multi-row inserts

⸻

⭐ 18. Troubleshooting

18.1 Common Problems
•	Too many parts
•	Slow merges
•	Out of memory
•	Long-running queries

18.2 Tools
•	system.errors
•	system.logs
•	TRACE log

⸻

⭐ 19. Best Practices — Лучшие практики ClickHouse
•	Использовать MergeTree для любых крупных таблиц
•	Максимально использовать ORDER BY правильно
•	Использовать LowCardinality для строковых полей
•	Проектировать sharding key заранее
•	Делать large batch inserts
•	Хранить данные в S3 как вторичное хранилище
•	Для кластеров — использовать ClickHouse Keeper
•	Отдавать предпочтение projections и skip indexes
•	Всегда мониторить количество parts и merges
•	Все конфигурации — через GitOps