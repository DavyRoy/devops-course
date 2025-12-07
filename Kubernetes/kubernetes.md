☸️ Kubernetes Roadmap — Полное структурированное описание всех тем (без пропусков)

⸻

⭐ 1. Introduction — Введение

1.1 Overview of Kubernetes — Обзор Kubernetes
•	Платформа для оркестрации контейнеров
•	Автоматизация деплоя, масштабирования и управления

1.2 Why use Kubernetes? — Зачем использовать Kubernetes
•	Высокая доступность
•	Автомасштабирование
•	Управление состоянием приложений
•	Self-healing

1.3 Key Concepts and Terminologies — Ключевые термины
•	Cluster
•	Node
•	Pod
•	Deployment
•	Service
•	Namespace
•	Control Plane / Worker Nodes

1.4 Kubernetes Alternatives — Альтернативы
•	Docker Swarm
•	HashiCorp Nomad
•	AWS ECS

⸻

⭐ 2. Containers — Контейнеры

(основа работы Kubernetes)
•	Контейнеры как единицы деплоя
•	Образы Docker/OCI

⸻

⭐ 3. Setting up Kubernetes — Установка Kubernetes

3.1 Deploying your First Application
•	Создание Deployment
•	Применение манифестов (kubectl apply)

3.2 Choosing a Managed Provider
•	EKS (AWS)
•	GKE (Google Cloud)
•	AKS (Azure)

3.3 Installing a Local Cluster
•	Minikube
•	Kind
•	K3s
•	MicroK8s

⸻

⭐ 4. Running Applications — Запуск приложений

4.1 Pods
•	Минимальная единица деплоя
•	Один или несколько контейнеров

4.2 ReplicaSets
•	Обеспечивают нужное число реплик Pod’ов

4.3 Deployments
•	Контролируют обновления и откаты
•	Декларативное управление

4.4 StatefulSets
•	Stateful-приложения
•	Стабильные имена
•	Персистентность

4.5 Jobs
•	Одноразовые задачи
•	CronJobs — по расписанию

⸻

⭐ 5. Services and Networking — Сервисы и сеть

5.1 External Access to Services
•	NodePort
•	LoadBalancer
•	Ingress

5.2 Load Balancing
•	Балансировка между Pod’ами

5.3 Networking & Pod-to-Pod Communication
•	CNI плагины
•	Pod network
•	ClusterIP сервисы

⸻

⭐ 6. Configuration Management — Управление конфигурациями

6.1 Injecting Pod Config with ConfigMaps
•	Конфигурации в виде переменных или файлов

6.2 Using Secrets for Sensitive Data
•	Пароли
•	Токены
•	TLS сертификаты

⸻

⭐ 7. Resource Management — Управление ресурсами

7.1 Setting Resource Requests and Limits
•	CPU
•	Memory
•	Ограничения qos classes

7.2 Assigning Quotas to Namespaces
•	Ограничение ресурсов namespace

7.3 Monitoring & Optimizing Resource Usage
•	Метрики CPU/Memory
•	Анализ потребления

⸻

⭐ 8. Security — Безопасность

8.1 Role Based Access Control (RBAC)
•	Roles
•	ClusterRoles
•	RoleBinding / ClusterRoleBinding

8.2 Network Security
•	NetworkPolicies
•	Ограничение трафика между Pod’ами

8.3 Container and Pod Security
•	PodSecurityPolicy (legacy)
•	Pod Security Standards (PSS)
•	SecurityContext

(Тема повторяется дважды в PDF — объединяем корректно)

⸻

⭐ 9. Monitoring and Logging — Мониторинг и логирование

9.1 Logs
•	kubectl logs
•	Системные логи

9.2 Metrics
•	cAdvisor
•	Metrics Server

9.3 Traces
•	Distributed tracing

9.4 Resource Health
•	Здоровье Pod’ов
•	readiness/liveness probes

9.5 Observability Engines
•	Prometheus
•	Grafana
•	OpenTelemetry

⸻

⭐ 10. Autoscaling — Автоматическое масштабирование

10.1 Horizontal Pod Autoscaler (HPA)
•	Масштабирование по CPU/Memory

10.2 Vertical Pod Autoscaler (VPA)
•	Изменение ресурсов Pod’а

10.3 Cluster Autoscaling
•	Авто-добавление нод

⸻

⭐ 11. Scheduling — Планирование

11.1 Basics — Основы
•	Как Kubernetes выбирает ноды

11.2 Taints and Tolerations
•	Ограничение запуска Pod’ов

11.3 Topology Spread Constraints
•	Распределение Pod’ов по зонам

11.4 Pod Priorities
•	Приоритеты Pod’ов

11.5 Evictions
•	Выселение Pod’ов при нехватке ресурсов

⸻

⭐ 12. Storage and Volumes — Хранение данных

12.1 CSI Drivers
•	Container Storage Interface

12.2 Stateful Applications
•	PersistentVolumes
•	PersistentVolumeClaims

⸻

⭐ 13. Deployment Patterns — Паттерны развёртывания

13.1 CI / CD Integration
•	Автоматизация деплоя

13.2 GitOps
•	FluxCD
•	ArgoCD

13.3 Helm Charts
•	Шаблоны приложений

13.4 Canary Deployments
•	Постепенное развертывание

13.5 Blue-Green Deployments
•	Два окружения (blue и green)

13.6 Rolling Updates / Rollbacks
•	Плавные обновления
•	Резервные откаты

⸻

⭐ 14. Advanced Topics — Продвинутые темы

14.1 Creating Custom Controllers
•	control loops

14.2 Custom Schedulers and Extenders
•	Пользовательские планировщики

14.3 Custom Resource Definitions (CRDs)
•	Расширение API Kubernetes

14.4 Kubernetes Extensions and APIs
•	API Machinery
•	Admission Controllers

⸻

⭐ 15. Cluster Operations — Операции с кластерами

15.1 Should you manage your own Cluster?
•	Self-hosted vs cloud

15.2 Installing the Control Plane
•	API Server
•	Scheduler
•	Controller Manager

15.3 Adding and Managing Worker Nodes
•	kubelet
•	kube-proxy

15.4 Multi-Cluster Management
•	Federation
•	Управление несколькими кластерами

⸻

⭐ 16. Continue Learning — Продолжить обучение
•	DevOps Roadmap
•	Docker Roadmap
•	Backend Roadmap