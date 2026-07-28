DOM XSS![alt text](image.png)
![alt text](image-1.png)

Bonus payload ![alt text](image-2.png)
`<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/771984076&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>`

Витік конфіденційних даних
Спочатку шукаємо відкриті директорії, але отримуємо помилку: ![alt text](image-3.png)

Вносимо зміни, які нам рекомендовано, та знову запускаємо сканування ![alt text](image-4.png)

**Error Handling** пройдено ![alt text](image-5.png)

Переходимо за посиланням `http://localhost:3000/ftp` і бачимо декілька файлів ![alt text](image-7.png)

Пробуємо відкрити `suspicious_errors.yml` і бачимо помилку ![alt text](image-8.png)

Добавляємо %2500.md після .yml ![alt text](image-6.png)

Як результат - пройшли ще кілька завдань ![alt text](image-9.png)

## Злам акаунтів (Authentication)
Переходимо на сторінку Login
Вводимо у поле Email: `' or 1=1--` і будь-який пароль.

Завдання пройдено! ![alt text](image-10.png)

## Додаткове завдання (Exposed Metrics)

**Опис**: Find the endpoint that serves usage data to be scraped by a popular monitoring system.

Найпопулярнішою системою збору метрик є prometheus.

Переходимо по /metrics ![alt text](image-11.png)
Завдання пройдено! ![alt text](image-12.png)
