🟧 RabbitMQ Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в RabbitMQ

1.1 What is RabbitMQ?
	•	Брокер сообщений (Message Broker)
	•	Post Office для микросервисов
	•	Основан на AMQP 0.9.1
	•	Поддерживает MQ Patterns, персистентность, роутинг

1.2 Why RabbitMQ?
	•	Надёжная доставка сообщений
	•	Простой протокол
	•	Многоязычные клиенты
	•	Плагинная архитектура

1.3 RabbitMQ vs Kafka
	•	RabbitMQ → очереди, guaranteed delivery
	•	Kafka → event log, streaming
	•	RabbitMQ = task queues
	•	Kafka = event pipelines

⸻

⭐ 2. RabbitMQ Architecture — Архитектура

2.1 Core Components
	•	Producer
	•	Consumer
	•	Queue
	•	Exchange
	•	Binding
	•	Message Broker node

2.2 Message Flow

Producer → Exchange → Binding → Queue → Consumer

2.3 Broker & Clustering
	•	Single-node
	•	Multi-node cluster
	•	Classic Mirroring
	•	Quorum queues

⸻

⭐ 3. Installation & Setup — Установка

3.1 Local Installation
	•	DEB/RPM
	•	Windows installer
	•	macOS brew

3.2 Docker Setup
	•	rabbitmq:3-management (панель UI)

3.3 Kubernetes
	•	RabbitMQ Cluster Operator
	•	Helm charts

3.4 RabbitMQ Management UI
	•	Панель мониторинга
	•	Создание очередей
	•	Просмотр consumers
	•	Управление exchange

⸻

⭐ 4. AMQP Fundamentals — Основы протокола AMQP

4.1 Exchanges
	•	direct
	•	topic
	•	fanout
	•	headers

4.2 Bindings
	•	Routing keys
	•	Pattern matching

4.3 Queues
	•	durable
	•	exclusive
	•	auto-delete

4.4 Messages
	•	body
	•	headers
	•	priority
	•	expiration TTL

4.5 Delivery Modes
	•	persistent
	•	non-persistent

⸻

⭐ 5. Messaging Patterns — Паттерны RabbitMQ

5.1 Work Queue Pattern
	•	распределение задач
	•	round-robin delivery

5.2 Publish / Subscribe
	•	fanout exchange

5.3 Routing
	•	direct exchange
	•	routing keys

5.4 Topics Pattern
	•	topic exchange
	•	wildcard keys (*, #)

5.5 RPC Pattern
	•	RPC через reply queues
	•	correlation id

5.6 Dead Letter Pattern (DLX)
	•	Dead Letter Exchanges
	•	failed messages
	•	retries

⸻

⭐ 6. Reliability & Delivery Guarantees

6.1 Acknowledgements
	•	manual ack
	•	auto ack
	•	nack / reject

6.2 Message Durability
	•	durable queues
	•	persistent messages

6.3 Publisher Confirms
	•	подтверждение на уровне брокера

6.4 Consumer Prefetch
	•	prefetch=N
	•	ограничение нагрузки

6.5 RabbitMQ HA Options
	•	Classic Mirrored Queues (legacy)
	•	Quorum Queues (новый HA стандарт)

⸻

⭐ 7. Advanced Queue Types

7.1 Quorum Queues
	•	Рафт-алгоритм
	•	Лучший HA режим

7.2 Stream Queues
	•	аналог Kafka Streams
	•	сохранение событий в log segment

7.3 Priority Queues
	•	приоритеты сообщений

7.4 Lazy Queues
	•	сообщения хранятся на диске
	•	хороши для больших очередей

7.5 TTL Queues
	•	время жизни сообщений
	•	перезапись (requeue)

⸻

⭐ 8. RabbitMQ Plugins

8.1 Management Plugin
	•	Web UI
	•	API

8.2 Shovel Plugin
	•	перенос сообщений на другой RabbitMQ

8.3 Federation Plugin
	•	распределенная архитектура

8.4 MQTT Plugin
	•	MQTT поверх RabbitMQ

8.5 STOMP Plugin
	•	STOMP messaging

⸻

⭐ 9. Monitoring & Observability

9.1 Metrics
	•	connections
	•	channels
	•	consumers
	•	messages ready
	•	messages unacked

9.2 Monitoring Tools
	•	Grafana dashboards
	•	Prometheus exporter
	•	RabbitMQ management API

9.3 Logging
	•	rabbit@hostname.log
	•	connection logs
	•	channel logs

⸻

⭐ 10. RabbitMQ in Kubernetes

10.1 RabbitMQ Cluster Operator
	•	CRD: RabbitmqCluster
	•	автоматический provisioning

10.2 Persistence
	•	StatefulSets
	•	PVC templates

10.3 Scaling
	•	horizontal scaling через sharding
	•	HA через quorum queues

⸻

⭐ 11. Security

11.1 Authentication
	•	username/password
	•	LDAP / OAuth

11.2 Authorization
	•	vhosts
	•	permissions (configure/read/write)

11.3 TLS
	•	SSL/TLS для connections

11.4 Firewalls
	•	Inter-node traffic
	•	Client traffic

⸻

⭐ 12. Performance Tuning

12.1 Producers
	•	batch publishing
	•	confirms async mode
	•	compression

12.2 Consumers
	•	prefetch
	•	concurrency

12.3 Broker
	•	disk performance
	•	open file limits
	•	memory alarms

12.4 Hardware Scaling
	•	SSD
	•	CPU
	•	Cluster size

⸻

⭐ 13. RabbitMQ Administration

13.1 Policies
	•	политика на все очереди
	•	TTL
	•	HA mode
	•	max-length / max-size

13.2 Sharding
	•	распределение нагрузки
	•	отдельные queues для каждого partition

13.3 Virtual Hosts
	•	логическая изоляция

13.4 Users
	•	user creation
	•	tagging (administrator, monitoring, management)

⸻

⭐ 14. Integrations

14.1 With Microservices
	•	Node.js
	•	Go
	•	Java Spring AMQP
	•	Python pika

14.2 With Kubernetes Apps
	•	Helm charts
	•	Auto service discovery

14.3 With Data Pipelines
	•	Spark
	•	Flink
	•	Logstash

⸻

⭐ 15. Troubleshooting

15.1 Classic Issues
	•	High unacked messages
	•	Memory alarms
	•	Queue growth
	•	Slow consumers

15.2 Tools
	•	rabbitmq-diagnostics
	•	rabbitmqctl
	•	Web UI health checks

15.3 Debugging
	•	Check consumer lag
	•	Check channel state
	•	Evaluate prefetch

⸻

⭐ 16. Best Practices — Лучшие практики
	•	Использовать Quorum queues вместо mirrored
	•	Обязательно включать Publisher Confirms
	•	Устанавливать prefetch для consumers
	•	Создавать отдельные vhosts
	•	Не хранить гигантские очереди → использовать TTL / lazy
	•	Обязательно мониторить unacked messages
	•	Использовать Shovel / Federation для интеркластерных связок
	•	Хранить конфигурации RabbitMQ в Git (GitOps)
	•	В Kubernetes → всегда использовать Operator