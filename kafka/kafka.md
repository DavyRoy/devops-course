🟦 Kafka Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в Kafka

1.1 What is Kafka?
•	Распределённая стриминговая платформа
•	Pub/Sub брокер сообщений
•	Хранение событий в логах
•	Обработка потоков данных в реальном времени

1.2 Why Kafka?
•	Высокая пропускная способность
•	Горизонтальное масштабирование
•	Fault-tolerance
•	Низкая задержка
•	Широкая экосистема (Connect, Streams, ksqlDB)

1.3 Kafka Use Cases
•	Логирование событий
•	Метрики и телеметрия
•	Интеграция микросервисов
•	Мониторинг
•	Data pipelines
•	ETL и CDC

⸻

⭐ 2. Kafka Architecture — Архитектура Kafka

2.1 Core Components
•	Broker
•	Producer
•	Consumer
•	Topic
•	Partition
•	Offset

2.2 Distributed Architecture
•	Логи распределены по нодам
•	Репликация данных
•	Разделение нагрузки

2.3 Zookeeper (Kafka <= 3.3)
•	Управление кворумом
•	Хранение метаданных
•	Координация брокеров

2.4 Kraft Mode (Kafka без Zookeeper)
•	Новый built-in consensus
•	Raft-based

⸻

⭐ 3. Topics & Partitions — Топики и партиции

3.1 Topics
•	Каналы данных
•	Лог событий

3.2 Partitions
•	Горизонтальная масштабируемость
•	Параллельность обработки

3.3 Replication
•	replication factor
•	лидеры и фолловеры

3.4 Retention Policies
•	time-based
•	size-based
•	compacted topics

⸻

⭐ 4. Producers — Продюсеры

4.1 Sending Messages
•	async
•	sync

4.2 Producer Configs
•	retries
•	acks (0 / 1 / all)
•	linger.ms
•	batch.size
•	compression (snappy, gzip, lz4, zstd)

4.3 Message Keys
•	Определяют partition routing

4.4 Delivery Semantics
•	At most once
•	At least once
•	Exactly once

⸻

⭐ 5. Consumers — Консьюмеры

5.1 Consumer Groups
•	Балансировка нагрузки
•	Автоматическая координация

5.2 Offsets
•	auto vs manual commit
•	commit strategies

5.3 Consumer Rebalance
•	trigger conditions
•	partitions rebalance

5.4 Ordering Guarantees
•	Ordering per partition

⸻

⭐ 6. Kafka Internals — Внутреннее устройство

6.1 Log Segments
•	segment files
•	index files

6.2 Page Cache
•	Высокая скорость чтения диска

6.3 Replication Protocol
•	ISR (in-sync replicas)
•	Under-replicated partitions

6.4 Controller Broker
•	управляет распределением лидеров

⸻

⭐ 7. Kafka Connect — Интеграции и коннекторы

7.1 What is Kafka Connect
•	ETL pipeline для Kafka
•	Экспорт/импорт данных из внешних систем

7.2 Connector Types
•	Source Connectors
•	Sink Connectors

7.3 Popular Connectors
•	JDBC
•	Elasticsearch
•	S3/GCS
•	PostgresCDC (Debezium)

7.4 Single Message Transform (SMT)
•	преобразование данных на лету

⸻

⭐ 8. Kafka Streams API — Обработка стримов

8.1 What is Kafka Streams
•	Java-библиотека для real-time обработки

8.2 Streams Concepts
•	KStream
•	KTable
•	State Store

8.3 Operations
•	map/filter
•	joins
•	windowing

8.4 Exactly Once in Streams
•	EOS v2

⸻

⭐ 9. ksqlDB — SQL поверх потоков

9.1 What is ksqlDB
•	SQL-engine для Kafka Streams
•	Реализация потоковых представлений

9.2 Operations
•	CREATE STREAM
•	CREATE TABLE
•	JOINS
•	TIME WINDOWS

9.3 Materialized Views
•	Реактивные агрегаты

⸻

⭐ 10. Security — Безопасность Kafka

10.1 Authentication
•	SASL
•	SCRAM
•	Kerberos
•	OAuth

10.2 Authorization
•	ACLs (Access Control Lists)

10.3 Encryption
•	TLS
•	Encryption in transit

⸻

⭐ 11. Monitoring Kafka

11.1 Metrics
•	Broker metrics
•	Producer/Consumer metrics
•	Lag monitoring

11.2 Tools
•	Prometheus
•	Grafana
•	Burrow (consumer lag)
•	Kafka UI tools (AKHQ, Kafdrop)

11.3 Logs
•	server.log
•	state change log
•	GC logs

⸻

⭐ 12. Kafka in Kubernetes

12.1 Operators
•	Strimzi
•	Confluent Operator

12.2 Patterns
•	StatefulSets
•	Persistent Volumes

12.3 Auto-scaling
•	Horizontal scaling per partition

⸻

⭐ 13. Tuning & Performance

13.1 Producer Tuning
•	batch.size
•	linger.ms
•	compression

13.2 Consumer Tuning
•	fetch.min.bytes
•	max.poll.interval.ms

13.3 Broker Tuning
•	page cache
•	SSD vs HDD
•	heap vs off-heap

13.4 Partition Strategy
•	Fewer large partitions
•	Avoid extreme cardinality

⸻

⭐ 14. Kafka Storage & Retention

14.1 Retention Types
•	delete
•	compact

14.2 Log Compaction
•	last known value per key
•	ideal for CDC and configs

14.3 Tiered Storage (Kafka 3.x+)
•	Offload старых данных
•	Cheaper storage

⸻

⭐ 15. Kafka Reliability & HA

15.1 Replication and ISR
•	In-Sync Replicas

15.2 Min ISR Setting
•	защита от потери данных

15.3 Rack Awareness
•	распределение реплик по зонам

⸻

⭐ 16. Kafka Cluster Operations

16.1 Adding/Removing Brokers

16.2 Increasing Partitions

16.3 Rebalancing

16.4 Cluster Upgrades
•	Rolling upgrades

16.5 Backup & Restore
•	MirrorMaker 2
•	Backup tools

⸻

⭐ 17. Troubleshooting

17.1 Common Problems
•	Consumer lag
•	Under-replicated partitions
•	Zombie brokers

17.2 Tools
•	kafka-topics
•	kafka-consumer-groups
•	kafka-dump-log

⸻

⭐ 18. Best Practices — Лучшие практики
•	Использовать ключи для ordering
•	Иметь минимум 3 брокера
•	Не создавать слишком много partitions
•	Чёткое именование топиков
•	Мониторить consumer lag
•	Хранить конфигурации в GitOps
•	Использовать Strimzi в Kubernetes
•	Не допускать label explosion в Kafka Streams
•	Использовать schema registry (Avro/Protobuf)
