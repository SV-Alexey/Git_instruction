Урок по Git для будущих Python-программистов
Введение в Git
Git - это распределённая система контроля версий, которая позволяет:

Отслеживать изменения в коде
Совместно работать над проектами
Возвращаться к предыдущим версиям
Управлять разными ветками разработки
Установка Git
Windows: Скачайте с git-scm.com
Mac: brew install git
Linux (Ubuntu/Debian): sudo apt-get install git
Проверьте установку: git --version

Настройка Git
git config --global user.name "Ваше Имя"
git config --global user.email "ваш@email.com"
git config --global core.editor "code --wait"  # для VS Code
Основные команды Git
1. Создание репозитория
mkdir my_python_project
cd my_python_project
git init
2. Проверка состояния
git status
3. Добавление изменений
# Добавить конкретный файл
git add main.py

# Добавить все файлы
git add .

# Добавить с просмотром изменений
git add -p
4. Коммит изменений
git commit -m "Добавил основной скрипт Python"
5. Просмотр истории
git log
git log --oneline
git log --graph
Работа с ветками (branches)
# Создать новую ветку
git branch feature/new-algorithm

# Переключиться на ветку
git checkout feature/new-algorithm
# Или (новый синтаксис)
git switch feature/new-algorithm

# Создать и переключиться
git checkout -b feature/new-algorithm

# Слияние веток
git checkout main
git merge feature/new-algorithm
Работа с удалёнными репозиториями (GitHub/GitLab)
# Добавить удалённый репозиторий
git remote add origin https://github.com/ваш-логин/ваш-репозиторий.git

# Отправить изменения
git push -u origin main

# Получить изменения
git pull origin main

# Клонировать репозиторий
git clone https://github.com/ваш-логин/ваш-репозиторий.git
.gitignore для Python-проектов
Создайте файл .gitignore в корне проекта:

# Файлы Python
__pycache__/
*.py[cod]
*$py.class

# Virtual environment
venv/
.env/

# IDE
.vscode/
.idea/

# Логи и базы данных
*.log
*.sqlite3

# Файлы сборки и дистрибуции
build/
dist/
*.egg-info/
Практическое задание
Создайте новый Python-проект с простым скриптом (например, калькулятор)
Инициализируйте Git-репозиторий
Создайте .gitignore для Python
Сделайте несколько коммитов с разными изменениями
Создайте ветку для нового функционала, добавьте его и слейте с основной веткой
Создайте репозиторий на GitHub и загрузите туда свой проект
Полезные советы для Python-разработчиков
Делайте атомарные коммиты (одна логическая изменение = один коммит)
Пишите осмысленные сообщения коммитов
Используйте виртуальные окружения (venv) и добавляйте их в .gitignore
Для больших проектов рассмотрите использование git hooks (например, для автоматического тестирования)
Изучите GitHub Flow/Git Flow для командной работы
Дополнительные материалы
Официальная документация Git
Pro Git book
GitHub Guides
Learn Git Branching - интерактивный туториал
