# prometheus-metrics

Веб-сервис с эндпоинтом **GET /metrics** для отдачи метрик в формате Prometheus. Стек: библиотека prometheus, Autumn, Winow.

## Установка в свой проект

1. Выполните команду `opm install prometheus-metrics`.
2. Из корня своего проекта выполните:
   `prometheus-metrics embed ./<КаталогСКонтролами>`
   Команда скопирует контроллер в указанный каталог.
3. Обычно это тот же каталог, что и значение `winow.КаталогСПриложениями` в `autumn-properties.json`.

Эндпоинт **GET /metrics** будет доступен по адресу вашего приложения.

## Создать новый проект с метриками

1. Установить Winow и CLI: `opm install winow`, `opm install winow-cli`.
2. Создать проект: `winow init myapp`, затем `cd myapp`.
3. Установить prometheus-metrics: `opm install prometheus-metrics`.
4. Встроить контроллер: `prometheus-metrics embed ./<КаталогСКонтролами>` (каталог тот же, что в `winow.КаталогСПриложениями`).
5. Запустить приложение: `winow start`.
6. В браузере открыть `http://localhost:3333/metrics` — страница с текстом метрик в формате Prometheus.
7. Встроить собственные метрики с помощью библиотеки [prometheus](https://github.com/yellow-hammer/prometheus)

**Быстрая проверка:** `opm install prometheus-metrics`, затем `prometheus-metrics demo`. В браузере открыть `http://localhost:9200/metrics` — увидите текст метрик (счётчики, `app_up` и т.д.).

```sh
# HELP app_up Приложение запущено (1)
# TYPE app_up gauge
app_up 1
# HELP metrics_requests_total Число запросов к эндпоинту /metrics
# TYPE metrics_requests_total counter
metrics_requests_total 1
```

## Команды

| Команда | Описание                                                    |
|---------|-------------------------------------------------------------|
| `embed` | Копирует контроллер в каталог, указанный аргументом команды |
| `demo`  | Запуск демо-сервера.                                        |

Подробнее: [README](https://github.com/yellow-hammer/prometheus-metrics#readme).
