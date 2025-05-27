# Ansible Playbook

Этот репозиторий содержит Ansible playbook для установки и настройки двух компонентов:

- [Vector (роль vector-role)](https://github.com/Takarigua/vector-role.git)
- [Lighthouse (роль lighthouse-role)](https://github.com/Takarigua/lighthouse-role.git)

## Описание

Playbook устанавливает систему сбора логов Vector и веб-интерфейс Lighthouse на локальную машину. Все зависимости описаны в `requirements.yml`, роли подключаются из отдельных репозиториев.

## Состав

- `inventory.ini` — инвентори-файл (локальный хост)
- `site.yml` — основной playbook
- `requirements.yml` — подключение внешних ролей

## Запуск

```bash
ansible-galaxy install -r requirements.yml
ansible-playbook -i inventory.ini site.yml --ask-become-pass
