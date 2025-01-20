# Домашнее задание к занятию 14 «Средство визуализации Grafana»

## Задание 1

1. Запустил связку prometheus-grafan из папки help.
2. Авторизовался в системе.
3. Подключил в качестве источника данных prometheus.
4. Список подключенных Datasource:
   ![](https://github.com/Granit16/monitoring_03/blob/main/grafana.png)


## Задание 2

1. Изучил предложенные ресурсы.
2. Создал Dashboard с четырьмя панелями:
   - NodeExporter CPU Utilization: ```100 - (avg by (instance) (rate(node_cpu_seconds_total{job="nodeexporter",mode="idle"}[1m])) * 100)```
   - CPULA 1/5/15: ```node_load1, node_load5, node_load15```
   - Memory Free: ```node_memory_MemFree_bytes```
   - FS Free: ```node_filesystem_avail_bytes```

Скриншот получившейся Dashboard:
  ![](https://github.com/Granit16/monitoring_03/blob/main/dashboard.png)


## Задание 3

1. Для каждой панели создал подходящее правило alert.
2. Скриншот Dashboard c алертами:
![](https://github.com/Granit16/monitoring_03/blob/main/alerts.png)
   

## Задание 4

Сохранил JSON MODEL Dashboard в виде [https://github.com/Granit16/monitoring_01/blob/main/JSON Model.json](https://github.com/Granit16/monitoring_03/blob/main/JSON%20Model.json)

 
