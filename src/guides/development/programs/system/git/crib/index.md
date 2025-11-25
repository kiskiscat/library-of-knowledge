# Шпаргалка

## Базовый рабочий процесс

- git init — Инициализировать новый Git-репозиторий
- git clone [url] — Склонировать проект с GitHub
- git add [file] — Добавить конкретный файл в staged
- git add . — Добавить все изменения в staged
- git commit -m "сообщение" — Зафиксировать staged изменения
- git push origin [branch] — Отправить коммиты на удалённый репозиторий
- git pull origin [branch] — Получить последние изменения

## Работа с ветками

- git branch — Список всех веток
- git branch [name] — Создать новую ветку
- git checkout [branch] — Переключиться на ветку
- git merge [branch] — Слить ветку с текущей
- git branch -d [branch] — Удалить ветку локально
- git push origin --delete [branch] — Удалить ветку на удалённом репозитории

## История коммитов

- git log --oneline — Краткая история коммитов
- git log --graph --oneline --all — Визуальная история с ветками
- git show [commit] — Показать изменения конкретного коммита
- git diff — Показать несохранённые изменения
- git diff --staged — Показать staged изменения
- git blame [file] — Кто и когда изменял каждую строку

## Отмена изменений

- git reset --soft HEAD^ — Отменить коммит, оставить изменения в staged
- git reset --hard HEAD^ — Полностью удалить последний коммит
- git checkout -- [file] — Отменить изменения в рабочей директории
- git revert [commit] — Создать новый коммит, который отменяет изменения
- git clean -fd — Удалить неотслеживаемые файлы и папки

## Сотрудничество на GitHub

- git fork — Создать личную копию репозитория
- git remote add upstream [url] — Добавить оригинальный репозиторий как upstream
- git fetch upstream — Получить обновления с оригинального репозитория
- git push -u origin [branch] — Отправить ветку и привязать её к upstream
- git pull --rebase upstream main — Обновить fork через rebase

## Stash и очистка

- git stash — Временно сохранить изменения
- git stash pop — Восстановить последний stash
- git stash list — Просмотреть все stash
- git stash drop — Удалить последний stash
- git prune — Удалить недостижимые объекты

## Теги и релизы

- git tag [name] — Создать легковесный тег
- git tag -a [version] -m "сообщение" — Создать аннотированный тег
- git push origin --tags — Отправить теги на удалённый репозиторий
- git tag -d [name] — Удалить локальный тег
- git push origin --delete tag [name] — Удалить тег на удалённом репозитории

## Продвинутые инструменты

- git bisect — Бинарный поиск коммита с багом
- git rebase -i [commit] — Интерактивный rebase (правка истории)
- git cherry-pick [commit] — Применить конкретный коммит к текущей ветке
- git reflog — Показать журнал ссылок (инструмент восстановления)
- git worktree add — Добавить дополнительную рабочую директорию

## Конфигурация

- git config --global user.name "Имя" — Установить глобальное имя пользователя
- git config --global user.email "email" — Установить глобальный email
- git config --global core.editor "code --wait" — Сделать VS Code редактором по умолчанию
- git config --global alias.co checkout — Создать алиас для команды
- git config --list — Показать все настройки Git
