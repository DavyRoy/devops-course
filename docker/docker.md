🐳 Docker Roadmap — Полное структурированное описание всех тем (без пропусков)

⸻

⭐ 1. Introduction — Введение

1.1 What are Containers? — Что такое контейнеры
•	Изолированные окружения для приложений
•	Общий kernel, отдельные ресурсы

1.2 Why do we need Containers? — Зачем нужны контейнеры
•	Повторяемость среды
•	Портативность
•	Лёгкость деплоя

1.3 Bare Metal vs VMs vs Containers — Железо vs ВМ vs Контейнеры
•	Bare Metal — прямой доступ к железу
•	Виртуалки — полный образ ОС
•	Контейнеры — общая ОС, отдельная среда

1.4 Docker and OCI — Docker и спецификация OCI
•	OCI стандартизирует образы и рантаймы
•	Docker поддерживает OCI

⸻

⭐ 2. Underlying Technologies — Базовые технологии

2.1 Namespaces — Пространства имён
•	PID
•	NET
•	MNT
•	IPC
•	USER

2.2 cgroups — Контроль ресурсов
•	CPU
•	RAM
•	IO

2.3 Union Filesystems — Union-FS
•	OverlayFS / AUFS
•	Послойная структура образов

2.4 Just get the basic idea — базовое понимание
•	Эти технологии используются внутри Docker

⸻

⭐ 3. Installation / Setup — Установка и настройка

3.1 Docker Desktop (Win/Mac/Linux)
•	Готовая среда с GUI
•	Docker Engine + Compose

3.2 Docker Engine (Linux)
•	Нативная инсталляция
•	Работа без GUI

⸻

⭐ 4. Basics of Docker — Основы Docker

4.1 Images — Образы
•	Шаблоны для контейнеров
•	Immutable (неизменяемые)

4.2 Containers — Контейнеры
•	Запущенные экземпляры образов

4.3 Volumes — Томá
•	Хранение данных вне контейнера

4.4 Networks — Сети
•	Bridge / Host / None

⸻

⭐ 5. Using 3rd Party Container Images — Использование сторонних образов

5.1 Databases
•	PostgreSQL
•	MySQL
•	Redis
•	MongoDB

5.2 Command Line Utilities
•	BusyBox
•	Alpine
•	curl/wget tools

⸻

⭐ 6. Data Persistence — Хранение данных

6.1 Ephemeral Container Filesystem — Эфемерная ФС контейнера
•	Данные внутри контейнера исчезают

6.2 Volume Mounts — Томы
•	Docker-managed storage

6.3 Bind Mounts — Монтирование каталогов хоста
•	Связывание локальных директорий хоста

⸻

⭐ 7. Building Container Images — Создание образов

7.1 Dockerfiles
•	Инструкции:
•	FROM
•	RUN
•	COPY
•	CMD / ENTRYPOINT
•	EXPOSE

7.2 Efficient Layer Caching — Эффективное кеширование слоёв
•	Минимизация изменений по слоям

7.3 Image Size and Security — Размер и безопасность образа
•	Alpine base
•	Multi-stage builds
•	No root user

⸻

⭐ 8. Container Registries — Реестры образов

8.1 Dockerhub — Docker Hub
•	Официальный публичный реестр

8.2 Others (ghcr, ecr, gcr, acr, etc)
•	GitHub Container Registry
•	AWS ECR
•	Google GCR
•	Azure ACR

8.3 Image Tagging Best Practices — Правила тагирования образов
•	latest
•	semver
•	commit hash

⸻

⭐ 9. Running Containers — Запуск контейнеров

9.1 docker run
•	Базовый запуск
•	Параметры:
•	-d background
•	-p ports
•	-v volumes
•	--env переменные окружения

9.2 Runtime Configuration Options
•	CPU limit
•	Memory limit
•	Restart policies

9.3 docker compose
•	Мультосервисные приложения
•	docker-compose.yml

⸻

⭐ 10. Container Security — Безопасность контейнеров

10.1 Runtime Security — безопасность во время выполнения
•	Rootless Mode
•	seccomp
•	AppArmor
•	SELinux

10.2 Image Security — безопасность образов
•	Проверка уязвимостей
•	Минимизация образа
•	digital signatures

⸻

⭐ 11. Docker CLI — Командная строка Docker

11.1 Images
•	docker images
•	docker pull
•	docker rmi

11.2 Containers
•	docker ps
•	docker start/stop/restart
•	docker logs

11.3 Volumes
•	docker volume ls
•	docker volume prune

11.4 Networks
•	docker network ls
•	Создание сетей

⸻

⭐ 12. Developer Experience — Опыт разработчика

12.1 Hot Reloading — Горячая перезагрузка
•	docker-compose + bind mounts

12.2 Debuggers — Отладчики
•	VSCode devcontainers
•	remote debugging

12.3 Tests — Тестирование
•	Integration tests в контейнерах

12.4 Continuous Integration — CI/CD
•	GitHub Actions
•	GitLab CI
•	Jenkins pipelines

⸻

⭐ 13. Deploying Containers — Деплой контейнеров

13.1 PaaS Options — PaaS-платформы
•	AWS ECS
•	Google Cloud Run
•	Azure Container Apps

13.2 Kubernetes
•	Полноценная оркестрация
•	Helm, StatefulSets, Ingress

13.3 Nomad
•	HashiCorp Nomad

13.4 Docker Swarm
•	Встроенный оркестратор Docker

⸻

⭐ 14. Continue Learning — Продолжить изучение

(по ссылкам из roadmap)
•	Kubernetes Roadmap
•	DevOps Roadmap
•	Backend Roadmap