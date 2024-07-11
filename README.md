# Домашнее задание к занятию «ELK» - `Скрыпников Илья`


### Задание 1. Elasticsearch
Установите и запустите Elasticsearch, после чего поменяйте параметр cluster_name на случайный.

Приведите скриншот команды 'curl -X GET 'localhost:9200/_cluster/health?pretty', сделанной на сервере с установленным Elasticsearch. Где будет виден нестандартный cluster_name.

Ответ : 

![Elasticsearch](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/4e01c614-2bd6-4e7b-a1a6-35e843f53b7c)


### Задание 2 Kibana
Установите и запустите Kibana.

Приведите скриншот интерфейса Kibana на странице http://<ip вашего сервера>:5601/app/dev_tools#/console, где будет выполнен запрос GET /_cluster/health?pretty.

Ответ:

![Elasticsearch2](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/cd3bf3e2-5598-4946-ba89-17a69af802e4)


### Задание 3 Logstash
Установите и запустите Logstash и Nginx. С помощью Logstash отправьте access-лог Nginx в Elasticsearch.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx.

Ответ :
![image](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/63bee2e9-898a-4cfb-9750-173d80cf2481)

   
### Задание 4 Filebeat.
Установите и запустите Filebeat. Переключите поставку логов Nginx с Logstash на Filebeat.

Приведите скриншот интерфейса Kibana, на котором видны логи Nginx, которые были отправлены через Filebeat.

Ответ :

![image](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/c608b2a2-c7ce-4625-b68b-dd5edb5723a2)

