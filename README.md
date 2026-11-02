# КР №2

Вариант 4. Сайт: https://kv.devops.local, порт приложения 8004.

- Приложение — Flask и Gunicorn, хранилище — Redis 7.
- Запуск на VM: `cd ~/kr2 && docker compose up -d`.
- Пароль создаётся только на VM в `.env`, права 600. В Git его нет.
- При доставке использовать `--exclude=.env --exclude=.git`.
- Nginx: `nginx/kr2.conf`; на сервере — `/etc/nginx/sites-available/kr2`.
- Проверка: `curl -4 --cacert ~/kr2.crt https://kv.devops.local/`.
- Данные хранятся в томе `kr2_redis_data`. Команду `down -v` не использовать.
- Дополнительное задание не выполнялось. PR остаётся открытым до защиты.

Шаблон: https://gitverse.ru/dgimatdinov/kr2-template
Исходный коммит: 3ee6c4bfda24df8cb4d61f8a27031813b3238338.
Исходный `.env` не импортирован; в `.env.example` оставлена заглушка.
