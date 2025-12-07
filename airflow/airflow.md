🟦 Apache Airflow Roadmap — Полное структурированное описание тем

⸻

⭐ 1. Introduction — Введение в Airflow

1.1 What is Apache Airflow?
•	Платформа оркестрации задач (workflow orchestration)
•	Написание DAG’ов на Python
•	Планирование, зависимости, ретраи

1.2 Use Cases — Где используют
•	ETL/ELT пайплайны
•	Data engineering / data warehousing
•	ML-пайплайны
•	Регулярные бэкапы и джобы

1.3 Airflow vs NiFi / Luigi / Prefect / DAGster
•	Airflow — кодовые DAG’и, батч-оркестрация
•	NiFi — потоковая, low-code
•	Prefect/DAGster — более современные конкуренты

⸻

⭐ 2. Architecture — Архитектура Airflow

2.1 Core Components
•	Webserver — UI
•	Scheduler — планировщик
•	Executor — выполнение задач
•	Workers — воркеры, выполняющие tasks
•	Metadata DB — хранение состояния DAG’ов

2.2 Executors
•	SequentialExecutor
•	LocalExecutor
•	CeleryExecutor
•	KubernetesExecutor
•	DockerExecutor

2.3 DAGs & Tasks
•	Directed Acyclic Graph (DAG)
•	Task — узел DAG
•	Operators — типы задач

⸻

⭐ 3. Installation & Setup — Установка и настройка

3.1 Local Installation
•	pip / pipx
•	airflow standalone

3.2 Docker / Docker Compose
•	Официальный docker-compose от Airflow

3.3 Kubernetes
•	Helm chart
•	Astronomer / Cloud Composer (managed Airflow)

3.4 Initial Configuration
•	airflow.cfg
•	Подключение к БД (Postgres/MySQL вместо SQLite)

⸻

⭐ 4. DAG Basics — Основы DAG’ов

4.1 DAG Definition
•	dag_id
•	default_args
•	schedule_interval
•	start_date
•	catchup

4.2 Tasks & Operators
•	PythonOperator
•	BashOperator
•	EmptyOperator

4.3 Dependencies
•	task1 >> task2
•	task1 << task2
•	chain(task1, [task2, task3], task4)

4.4 Scheduling
•	Cron expressions
•	Presets: @daily, @hourly, @once, @weekly

⸻

⭐ 5. Core Concepts — Ключевые концепции

5.1 DAG Run
•	Конкретный запуск DAG’а

5.2 Task Instance
•	Конкретное исполнение задачи

5.3 Execution Date
•	Логическое время запуска

5.4 Catchup
•	Догони прошлые периоды или нет

⸻

⭐ 6. Operators — Операторы

6.1 Built-in Operators
•	BashOperator
•	PythonOperator
•	EmailOperator
•	BranchPythonOperator
•	Dummy/EmptyOperator

6.2 Database Operators
•	PostgresOperator
•	MySqlOperator
•	MsSqlOperator

6.3 File / Cloud Operators
•	S3 operators
•	GCS operators
•	Local file operators

6.4 Sensors
•	ExternalTaskSensor
•	FileSensor
•	S3KeySensor
•	TimeSensor

6.5 Custom Operators
•	Написание своего оператора на Python

⸻

⭐ 7. Hooks & Connections — Подключения и хуки

7.1 Connections
•	Настройка connections через UI/Env vars
•	Types: HTTP, Postgres, MySQL, S3, GCP, AWS

7.2 Hooks
•	PostgresHook
•	MySqlHook
•	S3Hook
•	BaseHook

7.3 Secrets Backends
•	AWS Secrets Manager
•	GCP Secret Manager
•	HashiCorp Vault

⸻

⭐ 8. XCom & Data Passing — Передача данных между задачами

8.1 XCom Basics
•	push / pull
•	ti.xcom_push()
•	ti.xcom_pull()

8.2 When to Use XCom
•	Маленькие данные / метаданные
•	Не передавать большие объёмы

8.3 Alternatives
•	Хранить данные во внешнем хранилище (DB, S3, MinIO)

⸻

⭐ 9. Templates & Jinja — Шаблоны

9.1 Jinja Templating
•	{{ ds }}, {{ ds_nodash }}
•	{{ dag_run.conf }}

9.2 Macros
•	macros.datetime
•	macros.ds_add

9.3 Templates Fields
•	Какие поля в Operators подвержены шаблонизации

⸻

⭐ 10. Error Handling & Retries — Обработка ошибок

10.1 Retries
•	retries
•	retry_delay

10.2 SLA (Service Level Agreement)
•	sla для задач
•	SLA Miss callbacks

10.3 on_failure_callback / on_success_callback
•	Кастомная логика при ошибках/успехе

10.4 Trigger Rules
•	all_success
•	all_failed
•	all_done
•	one_success

⸻

⭐ 11. Airflow UI — Веб-интерфейс

11.1 Views
•	Graph View
•	Tree View
•	Gantt
•	Task duration

11.2 Managing DAGs
•	Pause/Unpause
•	Trigger DAG
•	Clear tasks

11.3 Logs
•	View logs per task instance

⸻

⭐ 12. Airflow in Production — Продакшн-сетап

12.1 Proper Executor
•	CeleryExecutor / KubernetesExecutor

12.2 External Database
•	Postgres / MySQL вместо SQLite

12.3 Log Storage
•	S3 / GCS / локальное хранилище

12.4 Multi-node Setup
•	Webserver
•	Scheduler
•	Workers
•	Flower (для Celery)

⸻

⭐ 13. Monitoring & Observability

13.1 Metrics
•	task_success / task_failed
•	scheduler delay
•	DAG run duration

13.2 Integrations
•	StatsD
•	Prometheus exporter
•	Grafana dashboards

13.3 Alerts
•	Email alerts
•	Slack notifications
•	PagerDuty через Webhooks

⸻

⭐ 14. Airflow & Data Platforms — Интеграции

14.1 Airflow + Kafka
•	Продюсеры/консьюмеры как задачи
•	Триггеры по offset’ам, batch jobs

14.2 Airflow + Spark
•	SparkSubmitOperator
•	Livy integration

14.3 Airflow + Databases / DWH
•	Snowflake
•	BigQuery
•	Redshift
•	PostgreSQL

14.4 Airflow + Cloud
•	GCP (Cloud Composer)
•	AWS MWAA
•	Azure Data Factory интеграции

⸻

⭐ 15. DAG Design Patterns — Паттерны проектирования

15.1 ETL / ELT Pipelines
•	Extract → Load → Transform

15.2 Fan-in / Fan-out
•	Параллельные ветки

15.3 Dynamic DAGs
•	Генерация задач по списку таблиц/ботов/конфигураций

15.4 Modular DAGs
•	Reusable functions / task groups

15.5 Task Groups
•	Логическая группировка задач

⸻

⭐ 16. Versioning & Deployment — Деплой DAG’ов

16.1 Git Repos
•	Всё в Git
•	GitOps подход

16.2 CI/CD for DAGs
•	Linting
•	Tests
•	Auto-deploy DAGs

16.3 Blue-Green / Canary
•	Плавное внедрение новых DAG версии

⸻

⭐ 17. Security — Безопасность Airflow

17.1 Authentication
•	Basic Auth
•	LDAP
•	OAuth / SSO

17.2 RBAC
•	Roles
•	Permissions
•	DAG-level access

17.3 Secrets Management
•	Через Secret backend

⸻

⭐ 18. Airflow 2.x Features — Современные фичи

18.1 TaskFlow API
•	Pythonic DAGs (decorators)

18.2 Smart Sensors
•	Оптимизация сенсоров

18.3 Better Scheduler
•	High-availability
•	Масштабирование

⸻

⭐ 19. Testing Airflow — Тестирование DAG’ов

19.1 Unit Tests
•	Тестирование Python-логики задач

19.2 DAG Integrity Tests
•	Проверка DAG на валидность

19.3 Local Task Run
•	airflow tasks test

⸻

⭐ 20. Best Practices — Лучшие практики
•	Хранить DAG’и в Git, с CI
•	Маленькие, читаемые DAG’и
•	Не передавать большие данные через XCom
•	Хранить бизнес-данные во внешних хранилищах
•	Наблюдать за scheduler lag и длительностью задач
•	Ограничивать max_active_runs и concurrency
•	Делать чёткую структуру папок DAG’ов
•	Использовать TaskFlow API и Task Groups
