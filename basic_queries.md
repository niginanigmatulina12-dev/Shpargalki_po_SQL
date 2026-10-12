## Добавление данных 
1. ALTER TABLE users ADD COLUMN address TEXT; - добавление столбца  
2. ALTER TABLE users RENAME TO app_users; - изменить название таблицы  
3. ALTER TABLE users DROP COLUMN address TEXT; - удалить столбец  
4. DROP TABLE <table_name>;  - удаление таблицы из базы данных  
5. DROP TABLE IF EXISTS <table_name>; - защита от ошибок при удалении таблицы  
6. INSERT INTO <table_name> (<field1>, <field2>, ...)  
VALUES (<value1>, <value2>, ...); - добавление данных в таблицу  
7. INSERT INTO app_users (username, email, created_at, age)  
VALUES  
('bob', 'bob@example.com', '2025-11-13 11:00:00', 18),  
('charlie', 'charlie@example.com', '2025-11-13 12:30:00', 20); - добавление несколько записей за один запрос  
8. INSERT INTO app_users (username, created_at)  
VALUES ('no_email_user', '2025-11-13 13:00:00'); - вставка с пропуском некоторых полей(Если какое-то поле может быть пустым (например, нам не всегда нужен email), его можно просто не указывать.
В этом случае id сгенерируется автоматически, а у email будет значение NULL.  




