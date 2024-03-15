# homework_lesson8
Провести настройку аутентификации доступа к yandex cloud-id, введя в консоли:

export YC_TOKEN=$(yc iam create-token)

export YC_CLOUD_ID=$(yc config get cloud-id)

export YC_FOLDER_ID=$(yc config get folder-id)

Ввести в консоли команды:

Инициализация terraform

terraform init

Проверка сценария

terraform terraform plan

Создание и настройка кластера описана wordpress в

https://github.com/gi949/homework_lesson4

Создание и настройка кластера OpenSearch и Dashboard описана в

https://github.com/gi949/homework_lesson7

Кластер kafka будем разворачивать на ВМ db1, db2 и db3.

Logstash будем разворачивать на ВМ db2.

Filebeat  будем разворачивать на ВМ lb1, lb2, bs1 и bs2.

Устанавливаем и настраиваем кластер kafka

ansible-playbook kafka_ins.yml

Подключаемся к ВМ db1 и проверяем создание топиков:

![kafka-1](https://github.com/gi949/homework_lesson8/assets/94520051/222c8256-9ab8-4954-b054-8e09c69d4bb3)

Устанавливаем и настраиваем logstash

ansible-playbook logstash_ins.yml

Устанавливаем и настраиваем агенты filebeats

ansible-playbook filebeats_ins.yml

Подключаемся к веб-интерфейсу Dashboards по <внешний ip:5601> под логином admin.

Проверяем, что логи от агентов поступают:

![all-ind](https://github.com/gi949/homework_lesson8/assets/94520051/67c52140-1cc3-45ee-9c09-c273a0586d9b)

Создаем индекс для логов из топика nginx

![nginx-1](https://github.com/gi949/homework_lesson8/assets/94520051/c7357132-2b40-4b2b-8a2a-d70a035fbf93)

![nginx-2](https://github.com/gi949/homework_lesson8/assets/94520051/7a509204-4df8-46f7-a40c-37d568dd670c)

![nginx-3](https://github.com/gi949/homework_lesson8/assets/94520051/5eb854fe-c540-4d93-9b1a-affdcdf3b6bd)

![nginx-4](https://github.com/gi949/homework_lesson8/assets/94520051/915b3b7f-94af-4c72-a7a4-6327832fdb0b)

В меню Discover смотрим логи nginx

![nginx-5](https://github.com/gi949/homework_lesson8/assets/94520051/b0955cc6-fb9f-4021-afd4-c21e25dc9b80)

Аналогично создаем индекс для логов из топика wordpress, в меню Discover смотрим логи wordpress

![wordpress-1](https://github.com/gi949/homework_lesson8/assets/94520051/fb5ad9f1-e698-4241-a3f1-93283f3567fd)

![wordpress-2](https://github.com/gi949/homework_lesson8/assets/94520051/55feae42-036e-4d42-a491-6cae9eced08a)





