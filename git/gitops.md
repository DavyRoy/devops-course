🔵 GitOps Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в GitOps

1.1 What is GitOps — Что такое GitOps
•	Методология управления инфраструктурой и приложениями через Git
•	Git = единый источник правды (“single source of truth”)
•	Автоматические синхронизации состояния в кластере

1.2 Why GitOps — Зачем использовать
•	Репродюсируемость
•	Аудит и история изменений
•	Безопасность и контроль доступа
•	Self-healing инфраструктуры

1.3 GitOps vs DevOps
•	GitOps = DevOps + declarative configs + automation through Git
•	DevOps → процессы
•	GitOps → автоматизация управления

⸻

⭐ 2. GitOps Core Principles — Основные принципы

2.1 Declarative Configuration
•	Всё описано в виде YAML
•	Kubernetes manifests
•	Helm charts
•	Terraform

2.2 Versioned & Immutable
•	Git хранит конфигурации
•	Коммиты = изменение инфраструктуры

2.3 Git is the Single Source of Truth
•	Всё, что в Git — истинная конфигурация

2.4 Continuous Reconciliation
•	Агент в кластере проверяет отклонения
•	Если кто-то применил изменения вручную → возврат

⸻

⭐ 3. GitOps Tooling — Инструменты GitOps

3.1 FluxCD
•	Kubernetes-native GitOps
•	Reconciliation loops
•	Kustomization controller
•	Helm controller

3.2 ArgoCD
•	Web UI
•	Application CRD
•	Multi-source sync
•	Health monitoring

3.3 Jenkins X
•	GitOps-first CI/CD

3.4 Terraform + GitOps
•	Git как управление IaC
•	Atlantis / Spacelift

3.5 Helm + GitOps
•	Управление версиями чартов через Git

⸻

⭐ 4. Git Repositories Structure — Структура репозиториев GitOps

4.1 App Repositories
•	Код + Dockerfile
•	CI pipelines
•	Charts/templates

4.2 Infra Repositories
•	Манифесты Kubernetes
•	Helm values
•	Kustomize overlays

4.3 Environments Repositories
•	dev
•	stage
•	prod
•	promotion через Git

⸻

⭐ 5. Deployment Models — Модели развертывания GitOps

5.1 Pull-Based GitOps
•	Агент в кластере сам забирает изменения
•	Flux / ArgoCD
•	Наиболее безопасная модель

5.2 Push-Based GitOps
•	CI/CD пушит изменения в кластер
•	Jenkins / GitLab CI
•	Менее безопасно

5.3 Hybrid
•	Push CI builds image
•	Pull CD deploys

⸻

⭐ 6. ArgoCD — GitOps через Argo

6.1 ArgoCD Components
•	API server
•	Repo server
•	Application controller

6.2 ArgoCD Concepts
•	Application
•	Sync policies
•	Health checks

6.3 ArgoCD Sync Strategies
•	Manual sync
•	Auto-sync
•	Prune
•	Self-heal

6.4 Multi-Cluster GitOps
•	Управление несколькими кластерами

⸻

⭐ 7. FluxCD — GitOps через Flux

7.1 FluxCD Architecture
•	Source Controller
•	Kustomize Controller
•	Helm Controller

7.2 Flux Workflows
•	GitRepository CRD
•	Kustomization CRD
•	HelmRelease

7.3 Secrets Management
•	SOPS
•	Sealed Secrets

⸻

⭐ 8. CI/CD Pipelines + GitOps

8.1 CI Responsibilities
•	Build
•	Test
•	Docker image
•	Push to registry

8.2 CD Responsibilities
•	Update manifest versions in Git
•	GitOps controller syncs changes

8.3 Promotion Between Environments
•	PR → dev
•	PR → stage
•	PR → prod

⸻

⭐ 9. GitOps with Kubernetes

9.1 Declarative Kubernetes
•	Deployments
•	Services
•	ConfigMaps
•	Secrets

9.2 Syncing State
•	Drift detection
•	Auto-correction

9.3 Multi-tenant Clusters
•	Namespaces
•	RBAC
•	NetworkPolicies

⸻

⭐ 10. GitOps Security — Безопасность

10.1 RBAC
•	Ограничения доступа
•	Только Git → источник конфигураций

10.2 Secret Management
•	SOPS
•	Vault
•	Sealed Secrets

10.3 Policy as Code
•	OPA Gatekeeper
•	Kyverno

10.4 Signed Commits / Signed Images
•	Sigstore
•	Cosign

⸻

⭐ 11. Observability in GitOps — Наблюдаемость

11.1 Monitoring Reconciliation
•	ArgoCD UI health checks
•	Flux events

11.2 Tracing Deployments
•	Jaeger / OpenTelemetry

11.3 Logs
•	GitOps controllers logs

⸻

⭐ 12. Rollouts — Стратегии выката

12.1 Blue-Green Deployments

12.2 Canary Deployments

12.3 Progressive Delivery
•	Argo Rollouts
•	Flagger (FluxCD)

12.4 Automated Rollbacks
•	Health checks
•	Metrics-based rollback

⸻

⭐ 13. GitOps in Cloud

13.1 EKS
•	GitOps с Argo / Flux
•	IRSA

13.2 GKE
•	Workload Identity
•	Config Sync

13.3 AKS
•	AAD integration

⸻

⭐ 14. GitOps Anti-Patterns — Ошибки
•	Прямое применение kubectl в прод
•	Хранение секретов в чистом виде
•	Push-based CD напрямую в кластер
•	Один монолитный репо без структурирования
•	Отсутствие среды dev/stage

⸻

⭐ 15. Best Practices — Лучшие практики
•	Всё декларативно
•	Весь CI/CD контролируется через Git
•	PR → единственный способ изменений
•	Использовать auto-sync только в dev
•	Secrets = только через SOPS/SealedSecrets
•	Хранить манифесты отдельно от приложения

⸻

⭐ 16. GitOps Hands-on — Практика

16.1 Build GitOps Repository
•	app repo
•	infra repo
•	environment repo

16.2 Deploy with ArgoCD
•	install Argo
•	create Application
•	sync

16.3 Deploy with FluxCD
•	bootstrap cluster
•	GitRepository + Kustomization

16.4 Progressive Delivery
•	Canary rollout via Flagger

⸻

⭐ 17. Advanced GitOps — Продвинутые темы

17.1 GitOps Orchestration
•	Multi-cluster GitOps
•	GitHub Actions → ArgoCD

17.2 Policy Driven GitOps
•	enforced constraints

17.3 GitOps + Terraform
•	Atlantis
•	Spacelift

17.4 GitOps + Helm
•	HelmRelease

⸻

⭐ 18. GitOps Ecosystem
•	ArgoCD
•	FluxCD
•	Argo Rollouts
•	Flagger
•	Jenkins X
•	SOPS
•	Sealed Secrets
•	Kyverno / OPA