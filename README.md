# Домашнее задание к занятию "`GitLab`" - `Мешков Сергей`
---

## Задание 1

### Выполненные этапы:

#### Шаг 1: Установка GitLab
- GitLab Community Edition успешно установлен на Ubuntu 24.04 LTS
- Доступен по адресу: http://10.0.2.15
- Все сервисы GitLab работают корректно

#### Шаг 2: Создание проекта
- Создан новый проект "my_project" в GitLab
- Проект настроен с публичным доступом

#### Шаг 3: Настройка GitLab Runner
- GitLab Runner зарегистрирован и запущен в Docker-контейнере
- Runner настроен для работы с Docker-in-Docker
- Использует образ golang:1.17 по умолчанию
- Назначен тег: netology

#### Настройки и статус Runner:
![Настройки Runner в проекте GitLab](img/Screenshot%from%2025-11-29%22-59-13.png)
![Детальная конфигурация Runner](img/Screenshot%from%2025-11-29%23-00-19.png)

#### Шаг 4: Связывание с локальным репозиторием
- Локальная директория связана с GitLab репозиторием
- Настроен remote: gitlab
- Код успешно пушится в репозиторий

## Задание 2

### Выполненные этапы:

#### Шаг 1: Перенос репозитория на GitLab
- Репозиторий `https://github.com/netology-code/sdvps-materials` перенесен на GitLab
- Создан проект `sdvps-materials`
- Код успешно запушен в GitLab
![Код успешно запушен в GitLab](Screenshot%from%2025-11-29%23-43-56.png)

#### Шаг 2: Создание .gitlab-ci.yml
Создан файл конфигурации CI/CD пайплайна:

```yaml
stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script:
   - go test .
  tags:
    - netology

build:
  stage: build
  image: docker:latest
  script:
   - docker build .
  tags:
    - netology
```

### Шаг 3: Результаты выполнения пайплайна

- Пайплайн успешно выполнен
- Оба этапа (test и build) завершены без ошибок
- Go тесты пройдены
- Docker сборка выполнена

### Скриншоты:

![Успешно выполненный пайплайн в GitLab CI/CD](img/Screenshot%from%2025-11-29%23-31-05.png)

![Детали выполнения этапа Jobe](img/Screenshot%from%2025-11-29%23-31-57.png)
