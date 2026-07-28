## ColdBox-VM

У браузері відкриваємо http://192.168.56.106 ![alt text](image.png)

Скануємо ![alt text](image-1.png)

Дізнаємося про трьох користувачів ![alt text](image-3.png)

Запускаємо брутфорс
`wpscan --url http://192.168.56.106/ -U c0ldd -P /usr/share/wordlists/rockyou.txt`
![alt text](image-2.png)

Входимо у wordpress ![alt text](image-4.png)

Замінюємо footer.php у редакторі тем на php reverse shell ![alt text](image-5.png)

Виконуємо команду `nc -lvnp 3421`

Після оновлення головної сторінки, отримуємо підключення ![alt text](image-6.png)

У файлі wp-config.php бачимо комбінацію користувача та паролю ![alt text](image-7.png)

Спробуємо зайти в сисетму під користовачем "c0dd" зі знайденим паролем: ![alt text](image-8.png)

У домашньому каталозі лежить файл user.txt ![alt text](image-9.png)

Визначимо, які саме повноваження є за допомогою команди: ![alt text](image-10.png) Ми можемо підвищити свої привілеї до root, використовуючи будь-яку з цих трьох команд

Використаємо vim

Запускаємо vim за допомогою sudo
`sudo vim -c ':!/bin/sh'`

![alt text](image-12.png)