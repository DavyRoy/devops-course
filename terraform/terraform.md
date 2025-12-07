🟩 Terraform Roadmap — Полное структурированное описание всех тем (по файлу)

(Mastering Terraform — roadmap from PDF)

⸻

⭐ 1. Introduction — Введение

(блок Introduction на диаграмме, верхняя часть страницы 1  ￼)

1.1 What is Terraform?

1.2 Usecases and Benefits — Применение и преимущества
•	Управление инфраструктурой
•	Автоматизация
•	Масштабирование

1.3 Installing Terraform — Установка Terraform

1.4 CaC vs IaC — Config-as-Code vs Infrastructure-as-Code
•	Понимание философии IaC

1.5 What is Infrastructure as Code? — Что такое IaC

⸻

⭐ 2. Hashicorp Configuration Language (HCL) — Язык конфигураций

(блок HCL на верхней правой части  ￼)

2.1 What is HCL — Что такое HCL

2.2 Basic Syntax — Базовый синтаксис HCL

⸻

⭐ 3. Terraform Providers — Провайдеры

(средняя часть диаграммы, блок “Providers” и его элементы  ￼)

3.1 Terraform Registry
•	Поиск провайдеров
•	Модули и ресурсы

3.2 Configuring Providers
•	provider “aws” {}, “azurerm”, “google”

3.3 Versions
•	Ограничения версий провайдеров

⸻

⭐ 4. Project Initialization — Инициализация проекта

(блок справа от Providers — “Project Initialization”  ￼)

4.1 terraform init
•	Инициализация проекта
•	Загрузка провайдеров

4.2 Directory structure
•	main.tf
•	variables.tf
•	outputs.tf

⸻

⭐ 5. Resources — Ресурсы

(один из основных узлов диаграммы, блок “Resources” и все дочерние элементы  ￼)

5.1 Resource Behavior — Поведение ресурсов

5.2 Resource Lifecycle — Жизненный цикл ресурсов

5.3 Meta Arguments
•	depends_on
•	count
•	for_each
•	provider
•	lifecycle

⸻

⭐ 6. Getting Started with Variables — Работа с переменными

(блок “Variables” по центру диаграммы  ￼)

6.1 Input Variables — Входные переменные

6.2 Type Constraints — Ограничение типов

6.3 Environment Variables — Переменные окружения

6.4 Variable Definition Files
•	*.tfvars

6.5 Validation Rules — Валидация

6.6 Local Values — Локальные значения

⸻

⭐ 7. Outputs — Выводы

(блок Outputs справа на диаграмме  ￼)

7.1 Output Syntax

7.2 Sensitive Outputs

7.3 Preconditions — Предусловия

⸻

⭐ 8. Format & Validate — Форматирование и валидация

(блок Format & Validate справа в середине  ￼)

8.1 terraform fmt

8.2 terraform validate

8.3 TFLint — линтер Terraform

⸻

⭐ 9. Deployment — Развертывание

(блок Deployment внизу справа  ￼)

9.1 terraform plan — План изменений

9.2 terraform apply — Применение изменений

⸻

⭐ 10. Inspect / Modify State — Управление состоянием

(большой левый блок State Management — часть “Inspect/Modify State”  ￼)

10.1 graph

10.2 list

10.3 output

10.4 show

10.5 rm / mv

10.6 -replace option in apply

10.7 state pull / state push

10.8 state replace-provider

10.9 state force-unlock

⸻

⭐ 11. Clean Up — Удаление инфраструктуры

(маленький блок Clean Up в центре  ￼)

11.1 terraform destroy

⸻

⭐ 12. State Management — Управление состоянием

(центральный блок “State” и все дочерние элементы  ￼)

12.1 State — Что такое tfstate

12.2 Remote State — Удаленное состояние

12.3 State Locking — Блокировка состояния

12.4 Sensitive Data — Чувствительные данные

12.5 Import Existing Resources — Импорт ресурсов

12.6 Splitting State Files — Разделение стейт-файлов

12.7 Versioning — Версионирование состояния

12.8 Best Practices for State — Лучшие практики

⸻

⭐ 13. Modules — Модули Terraform

(блок Modules в нижней середине диаграммы  ￼)

13.1 Root vs Child Modules — Корневые vs дочерние

13.2 Published Modules Usage — Использование опубликованных

13.3 Creating Local Modules — Создание локальных

13.4 Inputs / Outputs в модулях

13.5 Module Best Practices

⸻

⭐ 14. Provisioners — Провиженеры

(правый нижний блок “Provisioners” и темы вокруг него  ￼)

14.1 When to Use?

14.2 Creation-Time & Destroy-Time Provisioners

14.3 file provisioner

14.4 local-exec provisioner

14.5 remote-exec provisioner

14.6 Custom Provisioners

⸻

⭐ 15. Data Sources & Template Files

(правее Provisioners: “Data Sources” и “Template Files”  ￼)

15.1 Data Sources
•	data “aws_ami” …
•	data “template_file” …

15.2 Template Files
•	Шаблонные файлы
•	${} подстановка

⸻

⭐ 16. CI/CD Integration — Интеграция с CI/CD

(центр снизу на диаграмме  ￼)

16.1 GitHub Actions

16.2 Circle CI

16.3 GitLab CI

16.4 Jenkins

⸻

⭐ 17. Testing in Terraform — Тестирование

(правый низ диаграммы — блок Testing  ￼)

17.1 Unit Testing

17.2 Contract Testing

17.3 Integration Testing

17.4 End-to-End Testing

17.5 Testing Modules

⸻

⭐ 18. Scaling Terraform — Масштабирование

(нижний центр диаграммы — Scaling Terraform  ￼)

18.1 Splitting Large State — Разделение больших стейтов

18.2 Parallelism — Параллелизм

18.3 Deployment Workflow — Поток деплоя

18.4 Terragrunt — обертка над Terraform

18.5 Infracost — анализ стоимости

⸻

⭐ 19. Security — Безопасность

(левый нижний блок диаграммы  ￼)

19.1 Terrascan

19.2 Checkov

19.3 Trivy

19.4 KICS

⸻

⭐ 20. Secret Management — Управление секретами

(локация рядом со Security)
•	Vault
•	SOPS
•	KMS

⸻

⭐ 21. Compliance / Sentinel — Соответствие требованиям

(нижний блок безопасности)
•	HashiCorp Sentinel Policies
•	Policy-as-code

⸻

⭐ 22. HCP — HashiCorp Cloud Platform

(правый нижний угол диаграммы  ￼)

22.1 What & When to use HCP
•	Terraform Cloud / Enterprise

22.2 Enterprise Features
•	Private registries
•	Shared workspaces

22.3 Authentication — Аутентификация

22.4 Workspaces — Воркспейсы

22.5 VCS Integration — Интеграция с Git

22.6 Run Tasks — Пайплайны Terraform Cloud
