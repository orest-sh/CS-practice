## DeathNote-VM

На машині розгорнутий веб сервіс на порту 80 ![alt text](image.png)

Скануємо командою `dirsearch -u http://deathnote.vuln/` ![alt text](image-1.png)

В robots.txt бачимо файл important.jpg ![alt text](image-2.png)

Виконавши команду curl, отримуємо наступну підказку ![alt text](image-3.png)

Шлях до каталогу, де знаходяться файли user.txt і notes.txt є в коді сторінки ![alt text](image-4.png)

Використаємо їх для атаки методом підбору ![alt text](image-5.png)

В домашньому каталозі знаходимо user.txt ![alt text](image-7.png)
![alt text](image-8.png)

Шукаємо по всієї файловій системі файли та директорії, які мають в назві "kira":![alt text](image-9.png)

Наступна підказка у файлі case.wav ![alt text](image-11.png)

Декодуємо hex та base64 і отримуємо passwd : kiraisevil

Входимо під користувачем kira, який має права суперкористувача ![alt text](image-12.png)

Виводимо root.txt ![alt text](image-13.png)