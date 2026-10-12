## Добавление данных 
1. ALTER TABLE users ADD COLUMN address TEXT; - добавление столбца  
2. ALTER TABLE users RENAME TO app_users; - изменить название таблицы  
3. ALTER TABLE users DROP COLUMN address TEXT; - удалить столбец  
4. DROP TABLE 'table_name';  - удаление таблицы из базы данных  
5. DROP TABLE IF EXISTS 'table_name'; - защита от ошибок при удалении таблицы  
6. INSERT INTO 'table_name' ('field1', 'field2', ...)  
VALUES ('value1', 'value2', ...); - добавление данных в таблицу  
7. INSERT INTO app_users (username, email, created_at, age)  
VALUES  
('bob', 'bob@example.com', '2025-11-13 11:00:00', 18),  
('charlie', 'charlie@example.com', '2025-11-13 12:30:00', 20); - добавление несколько записей за один запрос  
8. INSERT INTO app_users (username, created_at)  
VALUES ('no_email_user', '2025-11-13 13:00:00'); - вставка с пропуском некоторых полей(Если какое-то поле может быть пустым (например, нам не всегда нужен email), его можно просто не указывать.
В этом случае id сгенерируется автоматически, а у email будет значение NULL.
## Обновление данных (UPDATE) 
1. Базовая конструкция  
<img width="770" height="87" alt="image" src="https://github.com/user-attachments/assets/a4944b1e-423a-4c57-b8ca-2b92ac83440a" />
2. UPDATE app_users  
SET username = 'new_name'  
WHERE id = 1;  
Два важных момента:  
•	команда меняет только те строки, которые подходят под условие WHERE  
•	если не указывать WHERE, изменятся все строки таблицы, без исключений
## Удаление данных (DELETE)
1. Базовая конструкция   
<img width="806" height="61" alt="image" src="https://github.com/user-attachments/assets/b9f6e12d-028b-4f81-b682-50de5dd2f451" />

2. DELETE FROM app_users WHERE id = 3;  
Если же выполнить запрос DELETE FROM app_users;, всё содержимое таблицы удалится, но сама структура таблицы будет прежней.  
Здесь правило то же, что и в UPDATE: обязательно используй WHERE, чтобы случайно не удалить всё.
<img width="808" height="419" alt="image" src="https://github.com/user-attachments/assets/7bf1cfdc-45fd-474e-ac8d-773845ac4c8f" />






