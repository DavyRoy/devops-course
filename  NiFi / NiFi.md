🟦 Apache NiFi Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в NiFi

1.1 What is Apache NiFi?
•	Платформа для потоковой обработки и маршрутизации данных
•	Low-code ETL/ELT
•	Drag-and-drop UI
•	Dataflow Automation

1.2 Why NiFi?
•	Простое построение data pipelines
•	Встроенная поддержка очередей и backpressure
•	Поддержка 300+ коннекторов
•	Гарантированная доставка FlowFiles
•	Подходит для Big Data, IoT, Kafka, databases

1.3 NiFi Ecosystem
•	NiFi
•	MiNiFi (edge agents)
•	NiFi Registry
•	NiFi Flow Management API

⸻

⭐ 2. Architecture — Архитектура NiFi

2.1 Core Concepts
•	FlowFile (единица данных)
•	FlowFile Attributes (метаданные)
•	Content Repository
•	FlowFile Repository
•	Provenance Repository

2.2 Key Components
•	Processors
•	Controller Services
•	Connections
•	Backpressure
•	Prioritizers

2.3 NiFi Cluster Architecture
•	Multi-node cluster
•	Zero-master architecture (coordinator + primary node)
•	Distributed dataflows

2.4 Flow Performance Concepts
•	Backpressure
•	Load balancing
•	Thread pools

⸻

⭐ 3. Installing NiFi — Установка

3.1 Installation Options
•	Binary package
•	Docker images
•	Kubernetes (helm charts)
•	Cloudera/Hortonworks distributions

3.2 Basic Configuration
•	nifi.properties
•	bootstrap.conf
•	JVM settings

3.3 NiFi UI Overview
•	Canvas
•	Processor palette
•	Connections
•	Queues
•	Appearance & configuration

⸻

⭐ 4. Processors — Процессоры (сердце NiFi)

4.1 What Are Processors?
•	Nodes in the dataflow
•	Execute actions on FlowFiles

4.2 Common Processor Types

Ingest:
•	GetFile / GetSFTP
•	GetHTTP
•	ConsumeKafka
•	ListenTCP/UDP

Transform:
•	UpdateAttribute
•	AttributesToJSON
•	JoltTransformJSON
•	ReplaceText

Route:
•	RouteOnAttribute
•	RouteOnContent
•	DetectDuplicate

Enrich:
•	LookupRecord
•	ExecuteScript

Output:
•	PutFile
•	PutSFTP
•	PutDatabaseRecord
•	PublishKafka

4.3 Processor Settings
•	Scheduling
•	Concurrent Tasks
•	Run Duration
•	Relationships (success/failure/etc.)

⸻

⭐ 5. FlowFiles — Основные единицы данных

5.1 FlowFile Structure
•	Content
•	Attributes (metadata)

5.2 FlowFile Lifecycle
•	Creation
•	Modification
•	Routing
•	Commit (Provenance)

5.3 FlowFile Provenance
•	Полная история обработки
•	Debug pipelines

⸻

⭐ 6. Connections, Queues & Backpressure

6.1 Connections
•	Связи между процессорами
•	Настройка load balancing

6.2 Queues
•	Внутреннее хранилище сообщений

6.3 Backpressure
•	По количеству FlowFiles
•	По размеру очереди
•	Защита от перегрузок

6.4 Prioritizers
•	Prioritize by age
•	By size
•	By attribute

⸻

⭐ 7. Controller Services

7.1 What Are Controller Services?
•	Reusable shared configurations

7.2 Common Services
•	SSLContextService
•	DBCPConnectionPool
•	RecordReader/Writer
•	Kerberos credentials

7.3 Best Practices
•	По максимуму использовать shared services

⸻

⭐ 8. Record-Oriented Processing

8.1 Record Reader / Writer
•	Avro
•	JSON
•	CSV
•	Parquet

8.2 Schema Registry Integration
•	Apache Schema Registry
•	Confluent Schema Registry

8.3 Record Processors
•	ConvertRecord
•	LookupRecord
•	UpdateRecord
•	QueryRecord

⸻

⭐ 9. Templates & Reusable Flows

9.1 Templates
•	Export/import flows
•	Сбор библиотек шаблонов

9.2 NiFi Registry
•	Версионирование flow’ов
•	Versioned flows
•	Rollback

9.3 Flow Reusability
•	Parameter Contexts
•	Dynamic flow creation

⸻

⭐ 10. Security

10.1 Authentication
•	LDAP
•	Kerberos
•	Single User Mode

10.2 Authorization
•	Policy-based security
•	User groups

10.3 TLS/HTTPS
•	Keystores
•	Truststores

10.4 Data-at-Rest
•	Encrypted repos (Content/FlowFile)

⸻

⭐ 11. Scripting & Extensions

11.1 ExecuteScript Processor
•	Python
•	Groovy
•	JavaScript

11.2 Custom Processors
•	Java SDK
•	Custom NiFi extensions

11.3 NiFi Expression Language
•	${filename}
•	${uuid()}
•	${now():format("yyyy-MM-dd")}

⸻

⭐ 12. Integrations — Интеграции NiFi

12.1 Kafka
•	ConsumeKafka
•	PublishKafka
•	Record-oriented Kafka processing

12.2 Databases
•	JDBC (PutDatabaseRecord)
•	LookupRecord with DB cache

12.3 Cloud
•	AWS S3 processors
•	GCP
•	Azure Blobs

12.4 Big Data
•	HDFS
•	Hive
•	Spark integrations

12.5 HTTP APIs
•	InvokeHTTP
•	ListenHTTP
•	REST integration

⸻

⭐ 13. NiFi in Kubernetes

13.1 Helm Charts
•	Stateful NiFi clusters

13.2 NiFi Operator
•	Automated cluster lifecycle

13.3 Persistent Storage
•	SSD volumes for repos

13.4 Horizontal Scaling
•	Add/remove nodes dynamically

⸻

⭐ 14. Performance & Tuning

14.1 JVM Tuning
•	Heap
•	GC settings

14.2 Repository Optimization
•	content repo storage type
•	cleaning tuning

14.3 High Throughput Flows
•	Increase concurrency
•	Distributed flows
•	Use record processors

14.4 Backpressure Strategies
•	Flow segmentation
•	Buffering patterns

⸻

⭐ 15. Monitoring & Observability

15.1 Built-In NiFi Monitoring
•	Provenance graphs
•	Data lineage
•	Flow statistics

15.2 External Monitoring
•	Prometheus metrics
•	Grafana dashboards

15.3 Logs
•	nifi-app.log
•	nifi-bootstrap.log

⸻

⭐ 16. Error Handling & Retry Logic

16.1 Routing to Failure
•	success / failure relationships

16.2 Dead Letter Queues
•	Custom DLQ patterns

16.3 Retries
•	Retry loops
•	Backoff strategies

⸻

⭐ 17. NiFi Cluster Management

17.1 Configuring Clusters
•	Zookeeper (NiFi < 1.14)
•	Embedded coordination (NiFi 1.14+)

17.2 Node Coordination
•	Primary node only processors
•	Stateless nodes

17.3 Rolling Updates
•	Zero-downtime pipelines

⸻

⭐ 18. NiFi Stateless (Advanced)

18.1 Stateless Mode
•	No state / no repos
•	Lightweight execution

18.2 Kubernetes-Friendly Dataflows
•	Stateless Docker flows

18.3 Integration with Function-as-a-Service
•	Lambda
•	Cloud Run

⸻

⭐ 19. Troubleshooting

19.1 Common Issues
•	Backpressure blocking
•	Memory leaks
•	Queue stuck
•	Slow processors

19.2 Tools
•	Provenance viewer
•	Dataflow debugger
•	Thread dumps

⸻

⭐ 20. Best Practices — Лучшие практики NiFi
•	Использовать NiFi Registry для версионирования
•	Меньше скриптов → больше готовых процессоров
•	Никогда не допускать больших очередей
•	Использовать Record API
•	Группировать flow’ы в Process Groups
•	Контролировать cardinality в attributes
•	FlowFiles должны быть небольшими
•	Настраивать backpressure для стабильности
•	GitOps для NiFi registry flows