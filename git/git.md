🟦 Git & GitHub Roadmap — Полное структурированное описание всех тем (без пропусков)

⸻

⭐ 1. Learn the Basics — Основы Git

1.1 What is Version Control? — Что такое контроль версий
•	Отслеживание изменений
•	История проекта
•	Работа в команде

1.2 Why use Version Control? — Зачем он нужен
•	Безопасность
•	Восстановление изменений
•	Совместная работа

1.3 Git vs Other VCS — Git против SVN/Mercurial
•	Распределённая система
•	Локальная работа без сервера

1.4 Installing Git Locally — Установка Git
•	Windows
•	Linux
•	macOS

⸻

⭐ 2. What is a Repository — Репозиторий

2.1 git init — Создание репозитория

2.2 git config — Настройка пользователя
•	user.name
•	user.email

2.3 Local vs Global Config
•	--local
•	--global
•	--system

2.4 Repository Initialization — Инициализация
•	.git папка
•	структура Git

⸻

⭐ 3. Intro and Git Commands — Основы работы

3.1 Working Directory — Рабочая директория

3.2 Staging Area — Индекс

3.3 Committing Changes — Коммиты
•	git add
•	git commit

3.4 .gitignore — Игнорирование файлов
•	синтаксис шаблонов

3.5 Viewing Commit History — История коммитов
•	git log

⸻

⭐ 4. Branching Basics — Ветвление

4.1 Creating Branch — Создание ветки

4.2 Renaming Branch — Переименование

4.3 Deleting Branch — Удаление

4.4 Checkout Branch — Переключение

⸻

⭐ 5. Merging Basics — Основы merge
•	git merge
•	fast-forward merge
•	merge commit

⸻

⭐ 6. Basic Collaboration — Базовая совместная работа

6.1 Git Remotes — Работа с удалёнными репо
•	origin
•	upstream

6.2 Managing Remotes — Управление remote
•	git remote add
•	git remote remove

6.3 Pushing / Pulling Changes — Отправка/получение
•	git push
•	git pull

6.4 Fetch without Merge — git fetch
•	получаем изменения без merge

⸻

⭐ 7. GitHub Essentials — Основы GitHub

7.1 Creating Account — Создание аккаунта

7.2 GitHub Interface — Интерфейс

7.3 Setting up Profile — Настройка профиля

7.4 Creating Repositories — Создание репо

7.5 Profile Readme — README на профиле

7.6 Private vs Public — Приватные / публичные

⸻

⭐ 8. Collaboration on GitHub — Работа над проектами

8.1 Forking vs Cloning — Форк и клонирование

8.2 Issues — Тикеты

8.3 Cloning Repositories — git clone

8.4 Pull Requests — Пул-реквесты

Подтемы:
•	PR from a Fork
•	Creating PR
•	Collaborators
•	Labelling Issues / PRs
•	Saved Replies
•	Mentions
•	Reactions
•	Commenting

⸻

⭐ 9. Merge Strategies — Стратегии слияний

9.1 Fast-Forward vs Non-FF

9.2 Handling Conflicts — Конфликты

9.3 Rebase — Перепись истории

9.4 Squash — Сквош коммитов

9.5 Cherry Picking Commits — cherry-pick

⸻

⭐ 10. Best Practices — Лучшие практики Git

10.1 Commit Messages — Сообщения коммитов

10.2 Branch Naming — Именование веток

10.3 PR Guidelines — Правила PR

10.4 Code Reviews — Code review

10.5 Contribution Guidelines — Руководство контрибьютора

10.6 Documentation — Документация
•	Markdown
•	Project Readme
•	GitHub Wikis

10.7 Clean Git History — Чистая история

⸻

⭐ 11. Working in a Team — Работа в команде

11.1 GitHub Organizations — Организации

11.2 Collaborators / Members — Роли

11.3 Teams within Organization — Команды

11.4 GitHub Projects — Проектные доски
•	Project Planning
•	Kanban Boards
•	Roadmaps
•	Automations

11.5 GitHub Discussions — Обсуждения

⸻

⭐ 12. Intermediate Git Topics — Средний уровень Git

12.1 Git Stash Basics — git stash

12.2 History — История Git

12.3 Linear vs Non-Linear — Линейная/нелинейная

12.4 HEAD — Указатель HEAD

12.5 Detached HEAD — Откреплённый HEAD

12.6 git log options — Опции историю

⸻

⭐ 13. Undoing Changes — Откат изменений

13.1 git revert — безопасный откат

13.2 git reset — жёсткий откат
•	–soft
•	–hard
•	–mixed

⸻

⭐ 14. Viewing Diffs — Просмотр различий

14.1 Between Commits

14.2 Between Branches

14.3 Staged Changes

14.4 Unstaged Changes

⸻

⭐ 15. Rewriting History — Перезапись истории

15.1 git commit –amend — исправление последнего коммита

15.2 git rebase — переназначение коммитов

15.3 git filter-branch — сложная перепись

15.4 git push –force — форс-пуш

⸻

⭐ 16. Tagging — Теги

16.1 Managing Tags

16.2 Pushing Tags

16.3 Checkout Tags

16.4 GitHub Releases

⸻

⭐ 17. Git Hooks — Хуки Git

17.1 What and Why?
•	Автоматизация задач

17.2 Client vs Server Hooks

17.3 Common Hooks
•	commit-msg
•	post-checkout
•	post-update
•	pre-commit
•	pre-push

⸻

⭐ 18. Submodules — Подмодули

18.1 Adding / Updating — Добавление/обновление

18.2 What and Why use? — Зачем нужны

⸻

⭐ 19. GitHub Workflow — GitHub Workflow

19.1 GitHub CLI
•	installation
•	issue management
•	repository management

19.2 GitHub Actions

Подтемы:
•	YAML Syntax
•	Workflow Triggers
•	Scheduled Workflows
•	Workflow Runners
•	Workflow Context
•	Secrets and Env Vars
•	Caching Dependencies
•	Storing Artifacts
•	Workflow Status
•	Marketplace Actions
•	Usecases — реальные сценарии

19.3 Git Patch — Патчи

⸻

⭐ 20. Advanced Git Topics — Продвинутый Git

20.1 Git Reflog — reflog

20.2 Git Bisect — поиск багов

20.3 Git Worktree — несколько рабочих деревьев

20.4 Git Attributes — атрибуты

20.5 Git LFS — Large File Storage

⸻

⭐ 21. GitHub Developer Tools — Инструменты GitHub Dev

21.1 REST API / GraphQL API

21.2 Creating Apps

21.3 GitHub Apps

21.4 OAuth Apps

21.5 Webhooks

⸻

⭐ 22. More GitHub Features — Дополнительные возможности GitHub

22.1 GitHub Sponsors

22.2 GitHub Pages — Статические сайты
•	Deploying Static Websites
•	Custom Domains
•	Static Site Generators

22.3 GitHub Gists — Сниппеты

22.4 GitHub Packages — Пакетный репозиторий

22.5 GitHub Codespaces — Облачная IDE

22.6 GitHub Education
•	Student Developer Pack
•	Classroom
•	Campus Program

22.7 GitHub Marketplace — Маркетплейс

22.8 GitHub Security

22.9 GitHub Models / Copilot
