# Задание 1
 Для выполнения задания по разработке Ansible playbook для запуска докеризированного веб-приложения, нам нужно создать несколько файлов: docker-compose.yml, Dockerfile для каждого сервиса, а также Ansible playbook, который будет управлять всеми этими компонентами. Давайте начнем поэтапно.
 - Шаг 1: Создание файлов Docker
   - Dockerfile.mysql
   - Dockerfile.nginx
   - Dockerfile.php
- Шаг 2: Создание docker-compose.yml
- Шаг 3: Создание конфигурационного файла для Nginx
- Шаг 4: Создание Ansible playbook
Создадим структуру для нашего Ansible проекта:
 project/
  - ├── docker-compose.yml
  - ├── Dockerfile.nginx
  - ├── Dockerfile.php
  - ├── Dockerfile.mysql
  - ├── nginx.conf
  - └── playbook.yml
- Шаг 5: Шаблон конфигурационного файла nginx (nginx.conf.j2)
Если потребуется использовать шаблон для конфигурации Nginx, создадим nginx.conf.j2:
- Шаг 6:Запуск Ansible playbook
Теперь, чтобы запустить playbook, используем команду:
   > ansible-playbook -i inventory playbook.yml
Где inventory - это файл с информацией о хостах:
    > [webservers]
    > your_server_ip ansible_user=your_user

Таким образом, мы создали структуру и плейбук для развертывания веб-приложения с использованием Ansible и Docker Compose.
