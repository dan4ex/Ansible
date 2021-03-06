<h1 align="center">Ansible</h1>
<p align="center">Рабочее решение по запуску Ansible</p>

<p align="center">
<a href="https://travis-ci.org/github/dan4ex/Ansible"><img src="https://travis-ci.org/dan4ex/Ansible.svg" alt="Build Status"></a>
<a href="https://github.com/dan4ex/Ansible"><img src="https://img.shields.io/github/forks/dan4ex/Ansible?style=social"></a>
<a href="https://github.com/dan4ex/Ansible"><img src="https://img.shields.io/github/stars/dan4ex/Ansible?style=social"></a>
<a href="https://github.com/dan4ex/Ansible"><img src="https://img.shields.io/github/watchers/dan4ex/Ansible?style=social"></a>
</p>

# Предварительная подготовка

1. В файле production указать спиcки серверов
2. Указать путь к вашему приватному ключу в group_vars/prod.yml
3. Установить ```$ pip install molecule yamllint ansible-lint docker```

# Тестирование ролей

1. Убедитесь что установлена тулза molecule версии 3 ```$ molecule --version```
2. Если не знаем что такое molecule, как с этим работать, ознакамливаемся -> [Ссылка](https://habr.com/ru/company/ostrovok/blog/448136/)
3. Прогоняем тесты:
```
$ cd roles/docker
$ molecule test
```
# Прогон ролей

Выполняем:

    $ ansible-playbook -i production site.yml
    
 **Готово**
