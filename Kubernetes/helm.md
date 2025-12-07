🟩 Helm Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в Helm

1.1 What is Helm — Что такое Helm
•	Пакетный менеджер для Kubernetes
•	Шаблоны YAML → Charts
•	Управление версиями развертываний

1.2 Why use Helm — Зачем нужен Helm
•	Уменьшение количества YAML-файлов
•	Повторное использование шаблонов
•	Удобный деплой приложений

1.3 Helm vs Kustomize
•	Helm = шаблоны + репозитории
•	Kustomize = патчи + overlays

⸻

⭐ 2. Helm Architecture — Архитектура Helm

2.1 Helm Client
•	CLI управление объектами

2.2 Tiller (Helm v2 — legacy)
•	Удалено в Helm 3

2.3 Helm 3 Architecture
•	Нет Tiller
•	Работа через Kubernetes API
•	Повышенная безопасность

⸻

⭐ 3. Setting Up Helm — Установка и настройка

3.1 Installing Helm
•	Linux/macOS: curl + tar
•	Windows: Chocolatey

3.2 Adding Repositories
•	helm repo add
•	helm repo list
•	helm repo update

3.3 Official Repositories
•	Bitnami
•	ArtifactHub

⸻

⭐ 4. Helm Charts — Основы Chart’ов

4.1 Chart Structure — Структура
•	Chart.yaml
•	values.yaml
•	templates/
•	charts/
•	README.md

4.2 Chart.yaml
•	Имя
•	Версия
•	Апстрим

4.3 values.yaml
•	Конфигурации по умолчанию

4.4 Templates
•	Go Template Syntax
•	{{ .Values }}
•	{{ .Release }}
•	{{ .Chart }}

⸻

⭐ 5. Template Engine — Шаблонный движок Helm

5.1 Go Templating Basics
•	if / else
•	range
•	pipelines

5.2 Sprig Functions
•	default
•	toYaml
•	indent

5.3 Template Helper Files
•	_helpers.tpl

⸻

⭐ 6. Working With Charts — Работа с чартами

6.1 Installing Charts
•	helm install

6.2 Upgrading
•	helm upgrade

6.3 Uninstalling
•	helm uninstall

6.4 Dry Run
•	helm install --dry-run --debug

6.5 Rollbacks
•	helm rollback

⸻

⭐ 7. Chart Development — Разработка чартов

7.1 Creating Charts
•	helm create

7.2 Customizing values
•	-f custom-values.yaml

7.3 Linting
•	helm lint

7.4 Packaging
•	helm package

7.5 Chart Versions
•	Semantic Versioning

⸻

⭐ 8. Helm Repositories — Репозитории Helm

8.1 Hosting Your Own Repo
•	GitHub Pages
•	S3 Bucket

8.2 Pushing Charts
•	chartmuseum
•	helm push

8.3 Signing Charts
•	GPG
•	helm verify

⸻

⭐ 9. Advanced Helm — Продвинутые темы

9.1 Subcharts
•	charts/ directory

9.2 Global Values
•	.Values.global

9.3 Hooks
•	pre-install
•	post-install
•	pre-upgrade

9.4 Helm Secrets
•	Шифрование values
•	SOPS

9.5 Helmfile
•	Оркестрация нескольких чартов

⸻

⭐ 10. Helm + Kubernetes + DevOps

10.1 Helm in CI/CD
•	GitLab CI
•	GitHub Actions
•	ArgoCD

10.2 GitOps with Helm
•	FluxCD + Helm Operator

10.3 Deploying Applications
•	Canary
•	Blue/Green
•	Multi-environment values
