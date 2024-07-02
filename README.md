# Old_Children_Weapon_Shop (OCWS)

Данная база данных разрабатывается чисто ради своего личного интереса и для изучения работы SQL кода. В первой версии, что была скинута 02.07.2024, содержится 8 таблиц, в которых есть некие данные.


# customers

Данная таблица представляет собой набор данных покупателей. Среди данных: 
- customer_id <-- индивидуальный идентификатор каждого покупателя
- second_name <-- Фамилия покупателя
- first_name <-- Имя покупателя
- surname <-- Отчество покупателя
 -status <-- Статус покупателя (пока не реализовано)


# products
Данная таблица представляет собой набор данных товаров. Среди данных: 
- product_id <-- индивидуальный идентификатор каждого товара
- product_name <-- название товара
- product_quantity <-- количество товара "на полке"
- category <-- категория товара
- price <-- цена товара

# orders
Данная таблица представляет собой набор данных заказов. Среди данных: 
- order_id <-- индивидуальный идентификатор каждого заказа
- customer_id <-- индивидуальный идентификатор каждого покупателя
- product_id <-- индивидуальный идентификатор каждого товара
- quantity <-- количество купленного товара
- order_date <-- дата заказа
- FOREIGN KEY (customer_id) REFERENCES customers(customer_id) <-- внешний ключ на столбец customer_id таблицы customers
- FOREIGN KEY (product_id) REFERENCES products(product_id) <-- внешний ключ на столбец product_id таблицы products

# employees
Данная таблица представляет собой набор данных работников магазина. Среди данных: 
- employee_id <-- индивидуальный идентификатор каждого работника
- second_name <-- Фамилия работника
- first_name <-- Имя работника
- surname <-- Отчество работника
- employee_position <-- Должность сотрудника
- experience <-- Опыт работы
- age <-- Возраст сотрудника
- wage <-- Заработная плата


# equipments
Данная таблица представляет собой набор данных оборудования. Среди данных: 
- equipment_id <--  индивидуальный идентификатор каждого оборудования
- equipment_name <-- название оборудования
- equipment_quantity <-- количество оборудования

# store
Данная таблица представляет собой набор данных магазинов. Среди данных: 
- store_id <-- индивидуальный идентификатор каждого магазина
- store_name <-- название магазина
- address <-- адрес магазина
- phone_number <-- внутренний телефонный номер магазина
- employees_number <-- количество работников магазина
- postcode <-- почтовый адрес магазина

# suppliers (не реализовано)
Данная таблица представляет собой набор данных поставщиков. Среди данных:
- supplier_id <-- индивидуальный идентификатор каждого поставщика 
- supplier_name <-- имя поставщика
- contact_person <-- контактное лицо поставщика


# warehouse (не реализовано)
Данная таблица представляет собой набор данных склада. Среди данных: 
- warehouse_id <-- индивидуальный идентификатор склада (не спрашивайте почему оно работает так, как работает)
- section_id <-- индивидуальный идентификатор каждого сектора
- product_id <-- индивидуальный идентификатор каждого товара
- products_in_stuck <-- количество товара "в стоке"
- FOREIGN KEY (product_id) REFERENCES products(product_id) <-- внешний ключ на столбец product_id таблицы products


