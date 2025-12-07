🔵 Prometheus Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в Prometheus

1.1 What is Prometheus? — Что это
•	Система мониторинга и алертов
•	Pull-модель сбора метрик
•	Сильная интеграция с Kubernetes
•	Работает через TSDB (time series database)

1.2 Why use Prometheus? — Зачем нужен
•	Метрики в реальном времени
•	Легкая интеграция с cloud-native сервисами
•	Дешёвый, быстрый, простой деплой
•	Гибкая система запросов (PromQL)

1.3 Prometheus Ecosystem
•	Alertmanager
•	Pushgateway
•	Grafana
•	Exporters
•	Thanos / Cortex / Mimir

⸻

⭐ 2. Architecture — Архитектура Prometheus

2.1 Core Components
•	Prometheus server
•	TSDB (база временных рядов)
•	Scrape Manager
•	Rules Engine (alerts / recording rules)

2.2 Pull Model
•	Prometheus сам ходит за метриками (scraping)
•	HTTP endpoint /metrics

2.3 Exporters
•	Node Exporter
•	Blackbox Exporter
•	MySQL/Postgres exporters
•	Kubernetes API exporter

2.4 Service Discovery
•	Kubernetes SD
•	Consul SD
•	EC2/GCE SD
•	Static configs

⸻

⭐ 3. Installing Prometheus — Установка

3.1 Binary Installation
•	Скачивание бинарников
•	Настройка systemd

3.2 Docker Deployment
•	prom/prometheus официальный образ

3.3 Kubernetes Deployment
•	Helm chart
•	kube-prometheus-stack

3.4 Prometheus Operator
•	CRD для:
•	ServiceMonitor
•	PodMonitor
•	Prometheus
•	Alertmanager
•	Thanos

⸻

⭐ 4. Configuration — Базовая конфигурация

4.1 prometheus.yml
•	global
•	scrape_configs
•	rule_files

4.2 Scrape Intervals
•	Использование scrape_interval
•	Разные интервалы для разных job’ов

4.3 Scrape Configs
•	static_configs
•	kubernetes_sd_configs
•	relabel_configs

4.4 Targets
•	Что такое target
•	Health targets
•	Проверка статуса

⸻

⭐ 5. Metrics — Метрики

5.1 Metric Types
•	Counter
•	Gauge
•	Histogram
•	Summary

5.2 Instrumentation
•	Клиентские библиотеки:
•	Go
•	Python
•	Java
•	Node.js

5.3 Labels
•	Ключевой элемент дизайна
•	cardinaility problems (избыточное количество label’ов)

5.4 Best Practices
•	Простые названия
•	Низкая кардинальность
•	Не логировать стеки ошибок в метрики

⸻

⭐ 6. PromQL — Язык запросов

6.1 Basic Queries
•	up
•	rate()
•	sum()
•	avg()
•	max()
•	min()

6.2 Operators
•	арифметика
•	логические операции
•	сравнения

6.3 Aggregation
•	sum by()
•	avg by()
•	max by()

6.4 Recording Rules
•	Запросы, которые сохраняют результаты
•	Ускорение сложных запросов

6.5 Query Best Practices
•	Использовать rate() для counter
•	Избегать суперсложных запросов в Grafana

⸻

⭐ 7. Exporters — Экспортёры

7.1 Node Exporter
•	CPU
•	RAM
•	Disk
•	Filesystem
•	Network

7.2 Blackbox Exporter
•	HTTP
•	DNS
•	ICMP
•	TCP

7.3 Database Exporters
•	Postgres
•	MySQL
•	MongoDB

7.4 Cloud Exporters
•	AWS
•	GCP
•	Azure

7.5 Custom Exporters
•	Собственные метрики через HTTP endpoint

⸻

⭐ 8. Alerting — Алерты

8.1 Alerting Rules
•	Определяются в rules.yml
•	Используют PromQL

8.2 Alert States
•	pending
•	firing

8.3 Alert Manager
•	Routing
•	Grouping
•	Templates

8.4 Notification Channels
•	Slack
•	Telegram
•	Email
•	PagerDuty
•	Webhooks

⸻

⭐ 9. Grafana Integration — Визуализация

9.1 Grafana Dashboards
•	Node exporter
•	Kubernetes dashboards
•	API latency dashboards

9.2 Datasource Configuration
•	Подключение Prometheus

9.3 Alerts in Grafana
•	Гибридный подход к алертам

⸻

⭐ 10. Kubernetes Monitoring — Мониторинг Kubernetes

10.1 kube-prometheus-stack
•	Самый популярный helm chart
•	Включает:
•	Prometheus
•	Operator
•	Grafana
•	node-exporter
•	alertmanager

10.2 ServiceMonitor
•	Оборачивает сервисы в мониторинг

10.3 PodMonitor
•	Мониторинг конкретных pod’ов

10.4 kube-state-metrics
•	Метрики состояния Kubernetes
•	Деплойменты, поды, ноды, PV, PVC

⸻

⭐ 11. Scaling & HA — Масштабирование и отказоустойчивость

11.1 Single Prometheus Instance (default)

11.2 Federation
•	Pull с других Prometheus инстансов

11.3 Sharding
•	Разделение по сервисам
•	Лучшая производительность

11.4 Long-term Storage
•	Thanos
•	Cortex
•	Mimir

11.5 Object Storage
•	S3 / MinIO
•	GCS

⸻

⭐ 12. Thanos — Расширение Prometheus

12.1 Why Thanos
•	Хранение данных на годы
•	Глобальный Prometheus view
•	Cross-cluster metrics

12.2 Thanos Components
•	Sidecar
•	Store Gateway
•	Querier
•	Compactor
•	Receiver

⸻

⭐ 13. Alerting Best Practices
•	Алерты только на actionable события
•	Избегать шума (alert fatigue)
•	Alert → dashboard → runbook
•	Алерты по SLO/SLA
•	Метрики golden signals:
•	Latency
•	Traffic
•	Errors
•	Saturation

⸻

⭐ 14. Security — Безопасность Prometheus
•	RBAC (в Kubernetes)
•	TLS для endpoints
•	Authentication proxy
•	Защита метрик
•	Ограничение внешнего доступа

⸻

⭐ 15. Performance & Optimization

15.1 Reduce Label Cardinality
•	Не использовать уникальные IDS в labels

15.2 Scraping Optimization
•	Правильные интервалы
•	Фильтрация target’ов

15.3 TSDB Tuning
•	Блоки хранения
•	Compression

⸻

⭐ 16. Troubleshooting
•	Проверка /targets
•	Проверка /rules
•	Ошибки scrape configs
•	Проблемы с label explosion

⸻

⭐ 17. Best Practices — Лучшие практики
•	Чистая схема именования метрик
•	Низкая кардинальность labels
•	Использовать ServiceMonitor
•	GitOps для конфигураций
•	Сохранять dashboards в Git
•	Long-term storage через Thanos/Cortex