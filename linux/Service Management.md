9.1 Creating New Services — Создание сервисов

Подтемы:
•	Что такое unit-файл (.service)
•	Расположение файлов:
•	/etc/systemd/system/ — пользовательские сервисы
•	/usr/lib/systemd/system/ — системные
•	Основные секции unit-файла:
•	[Unit] — описание, зависимости
•	[Service] — команда запуска, тип сервиса
•	[Install] — автозапуск
•	Типы сервисов:
•	simple
•	forking
•	oneshot
•	Команды для работы после создания:
•	systemctl daemon-reload
•	systemctl enable service
•	systemctl start service

⸻

9.2 Checking Service Logs — Проверка логов сервисов

Подтемы:
•	Основная команда:
•	journalctl -u service
•	Просмотр в реальном времени:
•	journalctl -u service -f
•	Ограничение вывода:
•	--since, --until
•	Просмотр общей системы:
•	journalctl -xe

⸻

9.3 Starting / Stopping Services — Запуск / остановка сервисов

Подтемы:
•	Запуск:
•	systemctl start service
•	Остановка:
•	systemctl stop service
•	Перезапуск:
•	systemctl restart service
•	Перезагрузка конфигурации без остановки:
•	systemctl reload service
•	Автозапуск:
•	systemctl enable service
•	Отключить автозапуск:
•	systemctl disable service

⸻

9.4 Checking Service Status — Проверка состояния сервисов

Подтемы:
•	Основная команда:
•	systemctl status service
•	Проверка всех сервисов:
•	systemctl list-units --type=service
•	Поиск “упавших” сервисов:
•	systemctl --failed
•	Проверка зависимостей:
•	systemctl list-dependencies service
•	Проверка настроек unit-файла:
•	systemctl cat service