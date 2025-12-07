🟧 Grafana Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в Grafana

1.1 What is Grafana?
•	Платформа визуализации и наблюдаемости
•	Поддерживает десятки источников данных
•	Используется с Prometheus, Loki, InfluxDB, Elastic и т. д.

1.2 Why Grafana?
•	Красивые и гибкие дашборды
•	Алерты
•	Query Builder
•	RBAC и multi-tenancy

1.3 Grafana Ecosystem
•	Grafana
•	Grafana Loki (логирование)
•	Grafana Tempo (tracing)
•	Grafana Mimir (metrics storage)
•	Grafana Cloud

⸻

⭐ 2. Installation & Setup — Установка и настройка

2.1 Installation Methods
•	Docker
•	Kubernetes (Helm chart)
•	Linux packages
•	Grafana Cloud

2.2 Basic Configuration
•	grafana.ini
•	SMTP (email alerts)
•	Auth (anonymous, OAuth, LDAP)

2.3 File Structure
•	dashboards/
•	plugins/
•	provisioning/

⸻

⭐ 3. Datasources — Источники данных

3.1 Popular Datasources
•	Prometheus
•	Loki
•	Elasticsearch
•	InfluxDB
•	PostgreSQL / MySQL
•	Tempo

3.2 Datasource Configuration
•	URL
•	Auth
•	Query settings

3.3 Provisioning Datasources
•	YAML provisioning
•	Автоматическая настройка Datasource в CI/CD

⸻

⭐ 4. Dashboards — Дашборды

4.1 Dashboard Basics
•	Панели (panels)
•	Ряды данных (queries)
•	Визуализации

4.2 Panels
•	Graph
•	Time Series
•	Stat
•	Gauge
•	Table
•	Logs panel
•	Heatmaps

4.3 Variables
•	Query variables
•	Interval variables
•	Custom lists
•	Chained variables

4.4 Dashboard JSON Model
•	Хранение и экспорт дашбордов
•	Версионирование в Git

4.5 Best Practices
•	Единая цветовая схема
•	Группировка панелей
•	Folder structure

⸻

⭐ 5. Queries — Запросы

5.1 Query Editors
•	Prometheus Query Builder
•	Elastic Query
•	SQL Query

5.2 Multi-query dashboards
•	Panels with multiple queries
•	Mixed datasources

5.3 Transformations
•	Merge
•	Filter
•	Group by
•	Rename
•	Math

5.4 Time Ranges
•	now-1h, now-24h
•	Dashboard-level time picker

⸻

⭐ 6. Alerts — Алерты в Grafana

6.1 Unified Alerting
•	Современная система алертов Grafana
•	Grafana Alerting вместо старых alerts

6.2 Alert Rules
•	Threshold alerts
•	Prometheus-based alerts
•	Multi-condition alerts

6.3 Contact Points
•	Email
•	Telegram
•	Slack
•	Webhooks
•	PagerDuty

6.4 Notification Policies
•	Routing
•	Alert grouping
•	Mute timing

6.5 Alert Rules Provisioning
•	YAML provisioning

⸻

⭐ 7. Grafana Loki — Логирование

7.1 What is Loki
•	Легковесная система логов
•	Метки как в Prometheus
•	Не индексирует весь текст

7.2 Loki + Grafana
•	Explore Mode
•	Logs panel
•	LogQL

7.3 Loki Components
•	Distributor
•	Ingester
•	Querier
•	Ruler
•	Gateway

⸻

⭐ 8. Grafana Tempo — Трейсы

8.1 What is Tempo
•	Tracing backend (OTLP)
•	Конкурент Jaeger и Zipkin

8.2 Tempo + Grafana
•	Trace-to-logs
•	Trace-to-metrics

8.3 Common Integrations
•	OpenTelemetry
•	Prometheus exemplars

⸻

⭐ 9. Grafana Mimir / Cortex — Длинное хранение метрик

9.1 Why Mimir
•	Massively scalable metrics storage
•	Long-term retention

9.2 Architecture Basics
•	Ingester
•	Querier
•	Store Gateway
•	Compactor

9.3 Integrations
•	Prometheus remote_write
•	Multi-cluster metrics

⸻

⭐ 10. Authentication & Security — Аутентификация и безопасность

10.1 User Management
•	Roles
•	Org
•	Teams

10.2 Authentication Providers
•	Basic Auth
•	OAuth
•	GitHub Login
•	Google SSO
•	Azure AD
•	LDAP

10.3 RBAC
•	Viewers
•	Editors
•	Admins

10.4 Audit Logs
•	История действий пользователей

⸻

⭐ 11. Provisioning — Автоматизация Grafana

11.1 Provisioning Dashboards
•	YAML provisioning
•	Автоматическая загрузка в CI/CD

11.2 Provisioning Alerts
•	alertmanager.yaml

11.3 Provisioning Plugins
•	plugin provisioning file

⸻

⭐ 12. Plugins — Плагины

12.1 Panel Plugins
•	Diagram
•	Plotly
•	Statusmap

12.2 Datasource Plugins
•	CloudWatch
•	Google BigQuery
•	Snowflake

12.3 App Plugins
•	Kubernetes App
•	Grafana Enterprise Features

12.4 Managing Plugins
•	grafana-cli plugins install ...

⸻

⭐ 13. Explore Mode — Режим изучения данных

13.1 Logs Explorer
•	Query builder
•	Live tail

13.2 Metrics Explorer
•	Raw PromQL queries

13.3 Traces Explorer
•	Tempo queries
•	Jump from metrics to traces

⸻

⭐ 14. Observability Platform — Платформа наблюдаемости

14.1 Logs + Metrics + Traces
•	Full observability
•	Unified dashboards

14.2 Golden Signals Dashboards
•	Latency
•	Traffic
•	Errors
•	Saturation

14.3 SLO Dashboards
•	SLO calculations
•	Error budgets

⸻

⭐ 15. High Availability & Scaling

15.1 Scaling Grafana
•	Multiple replicas
•	Shared database
•	Shared storage

15.2 External Databases
•	MySQL
•	PostgreSQL

15.3 Load Balancing
•	Ingress / reverse proxy

⸻

⭐ 16. Troubleshooting

16.1 Broken Dashboards
•	Query inspector
•	Check datasource health

16.2 Alert Errors
•	Debug alert evaluation logs

16.3 Explore Mode for Debugging
•	Compare raw queries

⸻

⭐ 17. Best Practices — Лучшие практики
•	Структурировать папки дашбордов
•	Использовать переменные везде, где возможно
•	Версионировать дашборды (GitOps)
•	Писать алерты по SLO, а не по CPU/Memory
•	Делать общие шаблоны дашбордов
•	Указывать единицы измерения (Units)
•	Использовать threshold’ы и annotations