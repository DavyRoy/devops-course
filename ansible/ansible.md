🟥 Ansible Roadmap — Полное структурированное описание тем

⸻

⭐ 1. Introduction — Введение

1.1 What is Ansible
•	Инструмент для управления конфигурациями и оркестрации
•	Agentless — без агентов на хостах
•	Использует SSH / WinRM

1.2 Why use Ansible
•	Простые YAML-плейбуки
•	Идемпотентность
•	Легкий вход для DevOps / админов

1.3 Ansible vs Puppet / Chef / Salt
•	Push-модель (от контроллера к нодам)
•	Нет демонов на клиентах

⸻

⭐ 2. Installation & Setup — Установка и настройка

2.1 Installing Ansible
•	Linux: пакетный менеджер
•	pip install ansible
•	ansible-core vs ansible

2.2 Control Node & Managed Nodes
•	Требования к control node
•	SSH-доступ к managed nodes

2.3 Basic Configuration
•	ansible.cfg
•	inventory по умолчанию

⸻

⭐ 3. Inventory — Инвентарь

3.1 Static Inventory
•	INI-формат
•	YAML-инвентарь

3.2 Groups & Children
•	Группы хостов
•	Вложенные группы

3.3 Host & Group Variables
•	host_vars/
•	group_vars/

3.4 Dynamic Inventory
•	Скрипты / плагины
•	AWS, GCP, Azure, Kubernetes и др.

⸻

⭐ 4. Ad-hoc Commands — Разовые команды
•	ansible all -m ping
•	ansible web -m shell -a "uptime"
•	Быстрая проверка соединения и простые задачи

⸻

⭐ 5. Playbooks — Плейбуки

5.1 Structure of a Playbook
•	hosts, tasks, vars, handlers
•	Несколько plays в одном файле

5.2 Tasks
•	Последовательное выполнение модулей

5.3 Idempotency
•	Повторяемый запуск без лишних изменений

⸻

⭐ 6. Modules — Модули Ansible

6.1 Core Modules
•	file, copy, template, user, service, package

6.2 OS-specific Modules
•	apt, yum, dnf, win_*

6.3 Cloud Modules
•	aws_, azure_, gcp_*

6.4 Custom Modules
•	Написание своих модулей на Python / Bash

⸻

⭐ 7. Variables & Facts — Переменные и факты

7.1 Variable Types
•	host/group vars
•	extra vars (-e)
•	vars в playbook

7.2 Facts
•	ansible_facts
•	setup module

7.3 Variable Precedence
•	Порядок приоритетов переменных

⸻

⭐ 8. Conditionals & Loops — Условия и циклы

8.1 when
•	Выполнение задачи при условии

8.2 with_items / loop
•	Перебор списков

8.3 register
•	Сохранение результата задачи

⸻

⭐ 9. Templates — Шаблоны (Jinja2)

9.1 Jinja2 Basics
•	{{ variable }}
•	{% if %}, {% for %}

9.2 template Module
•	Генерация конфигов из .j2

9.3 Filters
•	default, upper, to_nice_json и др.

⸻

⭐ 10. Handlers & Notifications — Обработчики
•	notify в tasks
•	handlers для restart/reload сервисов
•	Выполняются один раз, в конце play

⸻

⭐ 11. Tags — Теги
•	tags: у задач и plays
•	Запуск части плейбука: --tags, --skip-tags

⸻

⭐ 12. Error Handling — Обработка ошибок
•	ignore_errors: yes
•	failed_when
•	block / rescue / always

⸻

⭐ 13. Roles — Роли

13.1 Role Structure
•	tasks/, handlers/, templates/, files/, vars/, defaults/, meta/

13.2 Using Roles
•	roles: в playbook
•	Переиспользуемые куски логики

13.3 Role Best Practices
•	Одна роль — одна ответственность

⸻

⭐ 14. Ansible Galaxy — Экосистема ролей

14.1 galaxy.ansible.com
•	Поиск готовых ролей

14.2 ansible-galaxy CLI
•	ansible-galaxy init role_name
•	ansible-galaxy install

14.3 Collections
•	Наборы модулей + ролей + plugins

⸻

⭐ 15. Ansible Vault — Секреты
•	Шифрование чувствительных данных
•	ansible-vault create/edit/view
•	Использование в плейбуках
•	Интеграция с CI/CD (vault пароль как secret)

⸻

⭐ 16. Plugins — Плагины

16.1 Callback Plugins
•	Изменение вывода Ansible

16.2 Filter Plugins
•	Свои фильтры для Jinja2

16.3 Lookup Plugins
•	Чтение данных из внешних источников

⸻

⭐ 17. Testing Ansible — Тестирование

17.1 Molecule
•	Тестирование ролей
•	Локально через Docker/Podman/Vagrant

17.2 Integration Tests
•	Проверка итогового состояния
•	Testinfra / serverspec

⸻

⭐ 18. Ansible & CI/CD
•	Запуск плейбуков/ролей из GitLab CI / GitHub Actions / Jenkins
•	Использование dynamic inventory в пайплайнах
•	Шифрованные переменные (vault + secrets в CI)

⸻

⭐ 19. Performance & Scaling — Масштабирование
•	forks в ansible.cfg
•	Стратегии (linear, free)
•	async / poll
•	Управление большими инвентарями

⸻

⭐ 20. Ansible Tower / AWX — Веб-интерфейс и оркестрация

20.1 What is AWX / Ansible Tower
•	Web UI + REST API над Ansible

20.2 Features
•	RBAC
•	Инвентари
•	Креденшелы
•	Scheduled jobs

20.3 Usecases
•	Enterprise-окружения
•	Мульти-команды

⸻

⭐ 21. Network Automation — Сетевой Ansible
•	network_cli соединения
•	Модули для Cisco/Juniper/Arista
•	Управление конфигами сетевого железа

⸻

⭐ 22. Best Practices — Лучшие практики
•	Всё хранить в Git
•	Использовать роли и коллекции
•	Одинаковая структура репо
•	Минимум логики в плейбуках, больше в ролях
•	Никаких паролей в открытом виде — только vault
•	Чёткая структура env: dev / stage / prod