# Monitoring System for WordPress CMS

## Описание
Мониторинг CMS WordPress (PHP-FPM + MySQL + HAProxy) с использованием Prometheus и Grafana. Разворачивается через docker-compose. Необходимо добавить переменные в файл `.env` и `.my.cnf`

## Компоненты

| Компонент | Порт |
|-----------|------|
| WordPress + PHP-FPM | 9000 |
| MySQL | 3306 |
| HAProxy | 80 |
| Prometheus | 9090 |
| Grafana | 3000 |
| VictoriaMetrics | 8428 |

## Exporters

- node-exporter
- mysql-exporter
- php-fpm-exporter
- haproxy metrics
- blackbox-exporter

## ДЗ 
### Задание
    Для Prometheus необходимо установить отдельно хранилище метрик (VictoriaMetrics, Grafana Mimir, Thanos, и т. д.).
    Во время записи метрики в хранилище Prometheus должен дополнительно добавлять лейбл site: prod.

### Выполнение
     в конфиг файл  prometheus/prometheus.yml добавлено site: prod и remote_write
     в docker-compose добавлена victoria-metrics, глубина хранения 14 дней через переменную retentionPeriod

