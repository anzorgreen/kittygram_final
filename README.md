#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.
Стоит добавить ссылку на развернутый проект.
Необходимо добавить бейдж гитхаба, который свидетельствовал бы об удачно завершенном workflow
Чтобы проверить п.2 мне необходим доступ к репозиторию: ritisbarauskas
Необходимо добавить тут описание, чем отличаются продакш-версия от обычной. Когда и в каком случае нужно использовать ту или иную версию?
Нужна инструкция по развороту, как локальному, так и удаленному. При этом инструкция должна быть исчерпывающей.
Необходимо описание проекта.
Кто автор проекта?
Какие технологии используются?

#Kittygram Project

##This is a web-add collect cat photos in your account


[![Main Kittygram workflow](https://github.com/anzorgreen/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/anzorgreen/kittygram_final/actions/workflows/main.yml)



##The project is accessible at: kotikkotik.zapto.org

## Production vs. Development Versions

### Production
The production version is optimized for performance. It should be used in live environments where users access the system.

!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! ich must get only in branch "test-branch"
