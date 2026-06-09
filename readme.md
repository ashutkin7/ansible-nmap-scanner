# Ansible Nmap Scanner

Ansible-плейбук для автоматической установки Nmap и сканирования целей по 80-му порту.

## Структура проекта

*   `playbook.yml` — сценарий установки Nmap и сканирования.
*   `inventory.ini` — целевые хосты для выполнения плейбука.
*   `target.txt` — список адресов (целей) для сканирования.
*   `ansible.cfg` — конфигурация логирования.
*   `ansible.log` — лог-файл выполнения команд и плейбуков.

## Запуск

1.  Укажите хосты в `inventory.ini` и цели в `target.txt`.
2.  Выполните соответствующую команду:

**Тестовый прогон:**
```bash
ansible-playbook playbook.yml -i inventory.ini --check --diff
```

**Продуктовый запуск:**
```bash
ansible-playbook playbook.yml -i inventory.ini
```

*Результаты выполнения и логи записываются в файл `ansible.log`.*
