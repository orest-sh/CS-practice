# WebGoat: Hijack a session

Запускаємо контейнер WebGoat за допомогою Docker: ![](1.png)

У меню WebGoat відкриваємо вкладку Hijack a session ![](image.png)

За допомогою Burp Suite перехоплюємо невдалу спробу входу користувача ![](image-1.png)

У відповіді сервера бачимо значення `hijack_cookie` ![](image-2.png)

Використовуємо Burp Suite Intruder для підбору правильного значення `hijack_cookie` ![](image-4.png)

Завдання пройдено! ![](image-3.png)