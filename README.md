# Вычислитель отличий (Gendiff)

### Статус проекта и проверки:

[![CI](https://github.com/Slovuan-Swan/nodejs-gendiff-project/actions/workflows/ci.yml/badge.svg)](https://github.com/Slovuan-Swan/nodejs-gendiff-project/actions/workflows/ci.yml)
[![Quality gate status](https://sonarcloud.io/api/project_badges/measure?project=Slovuan-Swan_nodejs-gendiff-project&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=Slovuan-Swan_nodejs-gendiff-project)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=Slovuan-Swan_nodejs-gendiff-project&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=Slovuan-Swan_nodejs-gendiff-project)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Описание

**Gendiff** — это консольная утилита (CLI), которая сравнивает два конфигурационных файла и находит в них различия. Программа умеет работать с рекурсивными структурами данных любой глубины вложенности. Она поддерживает форматы **JSON** и **YAML**, а также предоставляет вывод в нескольких стилях.
В основе приложения лежит построение абстрактного дерева зависимостей (AST) и иммутабельный функциональный подход.

## Возможности

- Поддержка файлов конфигурации в форматах `.json`, `.yml`, `.yaml`.
- Рекурсивное сравнение вложенных объектов любой глубины.
- Три формата вывода результатов на выбор:
  - `stylish` (по умолчанию) — иерархический вид с отступами и маркерами `+` / `-`.
  - `plain` — плоский текстовый формат, описывающий путь до каждого изменения.
  - `json` — машиночитаемый структурированный формат данных.

## Установка

```bash
# Клонировать репозиторий
git clone https://github.com/Slovuan-Swan/nodejs-gendiff-project.git

# Перейти в папку проекта
cd nodejs-gendiff-project

# Установить зависимости
make install

# Связать пакет с системой для глобального использования команды gendiff
npm link
```

## Использование

```bash
# Вывод справочной информации
gendiff -h

# Сравнение файлов в формате stylish (по умолчанию)
gendiff __fixtures__/file1.json __fixtures__/file2.json

# Сравнение файлов в формате plain
gendiff -f plain __fixtures__/file1.json __fixtures__/file2.json

# Сравнение файлов в формате json
gendiff -f json __fixtures__/file1.json __fixtures__/file2.json
```

## Тестирование

```bash
make test
```

---

## Демонстрация работы (Asciinema)

### Сравнение плоских JSON файлов

[![asciicast](https://asciinema.org/a/1207728.svg)](https://asciinema.org/a/1207728)

### Поддержка плоских YAML файлов

[![asciicast](https://asciinema.org/a/1214100.svg)](https://asciinema.org/a/1214100)

### Рекурсивное сравнение (stylish)

[![asciicast](https://asciinema.org/a/1214302.svg)](https://asciinema.org/a/1214302)

### Вывод в формате Plain

[![asciicast](https://asciinema.org/a/1214651.svg)](https://asciinema.org/a/1214651)
