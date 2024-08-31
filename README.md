# Тестовое задание для DevOps Engineer.

## Описание задачи
  - Создать виртуальную машину на базе [Ubuntu 20.04](https://app.vagrantup.com/generic/boxes/ubuntu2004) с помощью [Vagrant](https://www.vagrantup.com/).
  - Настроить виртуальную машину через [Ansible](https://www.ansible.com/).
  - Создать отдельные контейнеры с [Prometheus](https://prometheus.io/) и [Grafana](https://grafana.com/) при помощи [docker-compose.yml](https://docs.docker.com/compose/compose-file/compose-file-v3/).
  - Добавить dashboard [Node Exporter Full](https://grafana.com/grafana/dashboards/1860-node-exporter-full/), который визуализирует метрики запущенной VM.
  - После выполнения команды `vagrant up` в браузере по адресу [http://localhost:3000](http://localhost:3000) должна открываться [Grafana](https://grafana.com/) с [Node Exporter Full](https://grafana.com/grafana/dashboards/1860-node-exporter-full/).

## Шаги

1. Создайте `Vagrantfile` для запуска виртуальной машины с операционной системой [Ubuntu 20.04](https://app.vagrantup.com/generic/boxes/ubuntu2004). +
2. Виртуальная машина должна подниматься с помощью команды `vagrant up`. +
3. Используйте [Ansible](https://www.ansible.com/) для провижионинга и настройки виртуальной машины. +
4. Настройте автозапуск [node_exporter](https://github.com/prometheus/node_exporter) на виртуальной машине. +
5. Установите и настройте [Grafana](https://grafana.com/) и [Prometheus](https://prometheus.io/) в контейнерах [Docker](https://docs.docker.com/) с помощью [Ansible](https://www.ansible.com/) и [docker-compose](https://docs.docker.com/compose/).
6. Настройте [Prometheus](https://prometheus.io/) для сбора метрик от [node_exporter](https://github.com/prometheus/node_exporter) и добавьте его в конфигурацию [Prometheus](https://prometheus.io/).
7. Добавьте автоматическое создание dashboard [Node Exporter Full](https://grafana.com/grafana/dashboards/1860-node-exporter-full/) в [Grafana](https://grafana.com/) для отображения основных метрик виртуальной машины.
