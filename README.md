Тестовое задание для DevOps Engineer.
Описание задачи
Создать виртуальную машину на базе Ubuntu 20.04 с помощью Vagrant.
Настроить виртуальную машину через Ansible.
Создать отдельные контейнеры с Prometheus и Grafana при помощи docker-compose.yml.
Добавить dashboard Node Exporter Full, который визуализирует метрики запущенной VM.
После выполнения команды vagrant up в браузере по адресу http://localhost:3000 должна открываться Grafana с Node Exporter Full.
Шаги
Создайте Vagrantfile для запуска виртуальной машины с операционной системой Ubuntu 20.04.
Виртуальная машина должна подниматься с помощью команды vagrant up.
Используйте Ansible для провижионинга и настройки виртуальной машины.
Настройте автозапуск node_exporter на виртуальной машине.
Установите и настройте Grafana и Prometheus в контейнерах Docker с помощью Ansible и docker-compose.
Настройте Prometheus для сбора метрик от node_exporter и добавьте его в конфигурацию Prometheus.
Добавьте автоматическое создание dashboard Node Exporter Full в Grafana для отображения основных метрик виртуальной машины.
