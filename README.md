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

## Exporters

- node-exporter
- mysql-exporter
- php-fpm-exporter
- haproxy metrics
- blackbox-exporter
