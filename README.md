# Домашнее задание к занятию "`GitLab`" - `Мешков Сергей`
---

## Задание 1

Все этапы задания выполнены успешно:
- Jenkins установлен и настроен
- Go установлен и работает
- Репозиторий подключен к Jenkins
- Тесты Go выполняются успешно
- Docker сборка работает корректно
- Сборка завершается со статусом SUCCESS

### Домашнее задание по Jenkins

### Выполнение задания

### Шаг 1: Установка Jenkins
Jenkins успешно установлен на Ubuntu VM и настроен.

### Шаг 2: Установка Go
Go версии 1.22.2 установлен на машину с Jenkins.

### Шаг 3: Создание форка репозитория
Создан форк репозитория: https://github.com/meshkov-sergey/sdvps-materials-cicd

### Шаг 4: Настройка Freestyle Project в Jenkins

#### Настройки проекта:
![Настройки Source Code Management](img/Screenshot%20from%202025-11-20%2022-09-35.png)

![Настройки Build Steps](img/Screenshot%20from%202025-11-20%2022-09-52.png)

#### Результаты выполнения сборки:
![Успешная сборка](img/Screenshot%20from%202025-11-20%2022-11-19.png)


## Задание 2: Pipeline Project

### Настройки Pipeline:
![Настройки Pipeline](img/Screenshot%20from%202025-11-21%2019-58-05.png)

### Stage View:
![Stage View](img/Screenshot%20from%202025-11-21%2019-58-39.png)

### Результаты выполнения:
![Console Output](img/Screenshot%20from%202025-11-21%2019-59-44.png)

### Вывод по заданию 2:
- Успешно создан Pipeline проект
- Сборка переписана на Declarative Pipeline
- Все этапы (Git, Test, Build Docker) выполняются последовательно
- Pipeline завершается со статусом SUCCESS
