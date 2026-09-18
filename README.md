<div align="center">

# Максим Москаленко

### Junior DevOps Engineer · Linux System Administrator

Linux-инфраструктура · Автоматизация · Контейнеры

[Telegram](https://t.me/matellabt) · [GitLab](https://gitlab.com/mosckalenckomaksim19-create) · [Docker Hub](https://hub.docker.com/r/xumuk595/devops-hello)

**Открыт к стажировке и junior-позиции**

</div>

---

Развиваюсь в DevOps и системном администрировании Linux. В собственной виртуальной лаборатории настраиваю серверы и сети, автоматизирую конфигурацию через Ansible и разворачиваю приложения в Docker и Kubernetes. Учусь в Российском университете транспорта по направлению «Инфокоммуникационные технологии и системы связи».

Мой опыт — учебная практика, pet-проекты и тестовые задания. Здесь собраны работы, которые можно изучить по коду, конфигурациям и результатам проверок.

## Избранные проекты

### 01 · Автоматизация Linux-инфраструктуры

**[WSL DevOps →](https://gitlab.com/mosckalenckomaksim19-create/wsl-devops)** · **[Ansible roles →](https://gitlab.com/mosckalenckomaksim19-create/ansible-roles)**

Лаборатория из двух Ubuntu Server 24.04 в VirtualBox с управлением из WSL2. Окружения `production` и `stage` разделены inventory и переменными; оба используются в учебном стенде.

- Автоматизация установки пакетов, hostname, timezone и swap через роль `common`.
- Настройки окружений в `group_vars`, отдельная роль `swaptrasher` для отключения и удаления swap.
- Разделение инфраструктуры и переиспользуемых ролей; загрузка ролей через `init.yml`.
- В локальной лаборатории: управление через пользователя `ansible`, SSH-ключи и `become`, установка Docker и Docker Compose отдельной ролью.

**Результат:** повторный запуск playbook для `stage` с ролями `common` и `docker` завершился с `changed=0`, `failed=0`. Последние локальные доработки могут опережать опубликованные версии на GitLab.

`Ansible` `Ubuntu Server` `YAML` `SSH` `Docker` `WSL2` `VirtualBox`

### 02 · HTTP-приложение в Docker и Kubernetes

**[devops-intern →](https://github.com/mosckalenckomaksim19-create/devops-intern)** · **[Образ в Docker Hub →](https://hub.docker.com/r/xumuk595/devops-hello)**

Выполненное тестовое задание: Python HTTP-сервис, Docker-образ и развёртывание в Minikube.

- Контейнер запускается от непривилегированного пользователя; приложение имеет endpoint `/healthz`.
- Deployment с двумя репликами, ClusterIP Service, readiness/liveness probes и requests/limits.
- В репозитории: инструкция запуска, схема архитектуры, скриншоты и результаты проверок.

**Результат:** Deployment `READY 2/2`, HTTP 200 от приложения и health endpoint; проверена обработка запросов обеими репликами через Service. Стенд работает на одном узле Minikube.

`Python` `Docker` `Kubernetes` `Minikube` `kubectl`

## Практика в лаборатории

| Область | С чем работал |
| --- | --- |
| Linux | Ubuntu Server, AlmaLinux, Bash, systemd, journalctl, пользователи, права и SSH |
| Диски и восстановление | LVM, snapshots, ext4/XFS, fstab, Rescue Mode, chroot, восстановление GRUB2 |
| Сети | IPv4, DNS, маршрутизация, Netplan, NAT/iptables; VLAN, DHCP и OSPF в учебных стендах |
| Облако | Базовая практика Yandex Cloud: виртуальная машина, Security Groups, Nginx и Object Storage |

## Куда развиваюсь

Углубляю знания Ansible, Docker и Kubernetes. Следующие направления — CI/CD и мониторинг инфраструктуры.

Ищу команду, где смогу применять навыки Linux-администрирования, разбирать реальные задачи и развиваться в автоматизации.

**Связаться: [@matellabt](https://t.me/matellabt)**
