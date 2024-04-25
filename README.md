# Домашнее задание к занятию 1 «Disaster recovery и Keepalived» - `Скрыпников Илья`


### Задание 1

![Схема](hsrp_hw.pkt)

![hw1_1](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/1dc24f2f-f352-44a0-aa79-bbfbc9ee36a7)
![hw1_2](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/ab372e23-cbe7-4745-bb53-bd4c2222181f)


### Задание 2
Скрипт bash
```
#!/bin/bash

if [[ $(ss -tuln | grep LISTEN | grep :80) ]] && [[ -f /var/www/html/index.html ]]; then
exit 0
else
exit 1
fi
```
```
Файл конфигурации keepalived
global_defs {
    enable_script_security
}
vrrp_script check_test {
    script "/etc/keepalived/keepaliv_script.sh"
    interval 3
    user root
}

vrrp_instance VI_1 {
    state MASTER
    interface enp0s8
    virtual_router_id 55
    priority 255
    advert_int 1

    virtual_ipaddress {
        192.168.123.9/24
        }
    track_script {
        check_test
        }
}
```
Скриншоты работы
![image](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/348c1538-4b27-470b-855f-1e0d8e2fe7ae)
![image](https://github.com/Skrypnikoviv/8-01hw/assets/162264420/cf31e775-cf1b-4a6a-bf83-91cac54089b5)
