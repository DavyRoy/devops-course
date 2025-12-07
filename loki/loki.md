🟦 Loki Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в Loki

1.1 What is Loki?
•	Система агрегации логов от Grafana Labs
•	Аналог Elasticsearch, но:
•	дешёвый
•	простой
•	масштабируемый
•	метки (labels) как в Prometheus

1.2 Why Loki?
•	Низкие требования к ресурсам
•	Интеграция с Prometheus
•	LogQL (похож на PromQL)
•	Отлично подходит для Kubernetes

1.3 Loki Ecosystem
•	Loki
•	Promtail
•	Grafana
•	Tempo (для трейсинга)
•	Mimir (для метрик)

⸻

⭐ 2. Loki Architecture — Архитектура Loki

2.1 Components
•	Distributor — принимает логи
•	Ingester — записывает в хранилище
•	Querier — выполняет запросы
•	Query Frontend — кеш, распределение запросов
•	Object Storage — S3 / GCS / MinIO
•	Index Store — индексация меток

2.2 How it Works
•	Логи → Promtail → Distributor → Ingester → Storage
•	Поиск → Query Frontend → Querier → Storage

2.3 Multi-Tenant Architecture
•	Multi-tenant ID
•	Изоляция данных

⸻

⭐ 3. Installing Loki — Установка Loki

3.1 Kubernetes
•	Loki Helm chart
•	kube-prometheus-stack
•	Loki Operator

3.2 Docker / Docker Compose
•	loki
•	promtail
•	grafana

3.3 Bare Metal / Binary
•	loki-linux-amd64
•	promtail-linux-amd64

⸻

⭐ 4. Promtail — Агрегатор логов

4.1 What is Promtail
•	Агент логов (аналог FluentBit / Filebeat)

4.2 Promtail Features
•	Tail файлов
•	Собирает Kubernetes логи
•	Преобразует и отправляет в Loki

4.3 Promtail Pipelines
•	parsing
•	regex / json / logfmt
•	labels mapping

4.4 Promtail Config
•	scrape_configs
•	pipeline_stages
•	static_config vs kubernetes_sd_configs

⸻

⭐ 5. LogQL — Язык запросов Loki

5.1 Log streams
•	label=value поиск
•	|= — точное совпадение
•	|~ — regex

5.2 Log Filtering
•	| logfmt
•	| json

5.3 Metrics from Logs
•	count_over_time()
•	rate()
•	sum by (label)

5.4 Pattern Parsing
•	pattern
•	regexp

5.5 Pipeline Stages
•	Парсинг
•	Tagging
•	Template

⸻

⭐ 6. Loki Configuration — Конфигурация

6.1 loki-config.yaml
•	server
•	ingester
•	distributor
•	querier
•	storage_config
•	schema_config

6.2 Storage Backends
•	S3
•	GCS
•	Azure Blob
•	MinIO

6.3 Retention
•	delete requests
•	retention policies
•	per-tenant retention

6.4 Compaction
•	Active index merging
•	Performance tuning

⸻

⭐ 7. Loki in Kubernetes

7.1 Loki via Helm chart
•	Single instance
•	Distributed mode

7.2 Promtail in Kubernetes
•	DaemonSet
•	Сбор логов по нодам

7.3 Pod Annotations
•	promtail.io/scrape
•	promtail.io/label

7.4 Kubernetes Labels
•	pod labels → Loki labels
•	namespace/service/workload logs

⸻

⭐ 8. Log Processing Pipelines

8.1 Parsing logs
•	logfmt
•	json
•	regex
•	multiline logs

8.2 Dropping logs
•	drop stage
•	rate limiting

8.3 Enriching logs
•	add labels
•	map fields to labels
•	timestamp override

⸻

⭐ 9. Loki Scaling & Performance

9.1 Single Binary Mode
•	Для тестовых сред

9.2 Distributed Mode
•	Массивная масштабируемость
•	HA

9.3 Sharding
•	Разделение запросов

9.4 Caching
•	Query frontend
•	Memcached cache

9.5 Index Optimization
•	Reducing label cardinality
•	Query optimization

⸻

⭐ 10. Alerting from Logs

10.1 Generating Metrics from Logs
•	Преобразование логов в метрики
•	Использование PromQL-like запросов

10.2 Alertmanager Integration
•	Alerts from Loki → Alertmanager

10.3 Grafana Alerts
•	Unified alerting
•	Custom alert rules

⸻

⭐ 11. Loki + Grafana Integration

11.1 Log Querying
•	query builder
•	filter logs by labels

11.2 Logs Panel
•	вывод логов с подсветкой

11.3 Explore Mode
•	logs + metrics + traces

11.4 Dashboard Integration
•	панель с логами
•	jump-to-logs feature

⸻

⭐ 12. Loki + Tempo — Tracing integration

12.1 Trace → Logs
•	Переход из трейсинга в логи

12.2 Logs → Traces
•	Поиск связанных трейсингов через exemplars

⸻

⭐ 13. Loki Security

13.1 Authentication & Authorization
•	reverse proxy
•	grafana auth
•	multi-tenant keys

13.2 TLS
•	HTTPS endpoints

13.3 Multi-Tenancy Isolation

⸻

⭐ 14. Observability for Loki Itself

14.1 Loki Metrics
•	Requests
•	Errors
•	Ingestion rate

14.2 Loki Dashboards
•	Grafana Loki dashboards

14.3 Log Volume Monitoring
•	Интенсивность логирования
•	Volume per service

⸻

⭐ 15. Troubleshooting

15.1 Common Issues
•	No logs in UI
•	Promtail not sending logs
•	Too many labels
•	Retention not applied

15.2 Tools
•	loki-canary
•	Query inspector
•	Promtail logs

⸻

⭐ 16. Best Practices — Лучшие практики Loki
•	Низкая кардинальность labels
•	Не класть user ID в labels
•	Логи = текст, не метрики
•	Использовать локальные SSD
•	Retention per environment
•	LogQL recording rules
•	GitOps для конфигов Loki