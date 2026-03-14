# prometheus-metrics

Веб-сервис с эндпоинтом **GET /metrics** для отдачи накопленных метрик в формате
[Prometheus Text Format](https://prometheus.io/docs/instrumentation/exposition_formats/). Стек: библиотека
[prometheus](https://github.com/yellow-hammer/prometheus), [Autumn](https://autumn-library.github.io/),
[Winow](https://autumn-library.github.io/winow/).

## Установка в свой проект (основной сценарий)

1. Выполните команду `opm install prometheus-metrics`.
2. Из корня своего проекта выполните:
   `prometheus-metrics embed ./<КаталогСКонтролами>`
   Команда скопирует контроллер в указанный каталог.
3. Обычно это тот же каталог, что и значение `winow.КаталогСПриложениями` в `autumn-properties.json`.

Эндпоинт **GET /metrics** будет доступен по адресу вашего приложения.

## Для разработчиков

- [CONTRIBUTING.md](CONTRIBUTING.md) — как внести вклад.
- [docs/release.md](docs/release.md) — как выпустить релиз.

## Лицензия

MIT License. Подробности см. в файле [LICENSE](LICENSE).

## Автор

Ivan Karlo (<i.karlo@outlook.com>)

При желании, отблагодарить автора можно по ссылке:

- [Boosty](https://boosty.to/1carlo/donate)
- [Чаевые](https://pay.cloudtips.ru/p/d752cb43)
