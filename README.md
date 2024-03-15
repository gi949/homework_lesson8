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

Создание и настройка кластера описана в

https://github.com/gi949/homework_lesson4

Создание и настройка кластера OpenSearch и Dashboard sописана в

https://github.com/gi949/homework_lesson7

Кластер kafka будем разворачивать на ВМ db1, db2 и db3.

Logstash будем разворачивать на ВМ db2.

Filebeat  будем разворачивать на ВМ lb1, lb2, bs1 и bs2.

Устанавливаем и настраиваем кластер kafka

ansible-playbook kafka_ins.yml

Подключаемся к ВМ db1 и проверяем создание топиков:

![kafka-1](https://github.com/gi949/homework_lesson8/assets/94520051/222c8256-9ab8-4954-b054-8e09c69d4bb3)

Устанавливаем и настраиваем кластер kafka






