| Сущность | Мнемоника | Описание понятия | Тип данных | Обязательность |
|:---|:---|:---|:---|:---|
| Клиент | client_id | Уникальный идентификатор клиента | INT | PK |
|  | full_name | ФИО клиента | VARCHAR(255) | NN |
|  | phone_number | Номер телефона клиента | VARCHAR(255) | NN |
|  | register_status | Есть ли у клиента ЛК | BOOL | NN |
|  | registration_date | Дата и время регистрации клиента | DATETIME | NN |
|  | channel | Предпочитаемый канал связи | VARCHAR(255) | NN |
| Сотрудники | employee_id | Уникальный идентификатор сотрудника | INT | PK |
|  | full_name | ФИО сотрудника | VARCHAR(255) | NN |
|  | phone_number | Номер телефона сотрудника | VARCHAR(255) | NN |
|  | job_title | Должность | VARCHAR(255) | NN |
|  | experience | Стаж работы | INT | NN |
| Услуга | service_id | Уникальный идентификатор услуги | INT | PK |
|  | category | Категория услуги | VARCHAR(255) | NN |
|  | name | Наименование услуги | VARCHAR(255) | NN |
|  | description | Описание услуги | VARCHAR(255) | NN |
|  | price | Цена услуги | INT | NN |
|  | service_time | Время оказания услуги | INT | NN |
| Начисление | accrual_id | Уникальный идентификатор начисления | INT | PK |
|  | client_id | Уникальный идентификатор клиента | INT | NN |
|  | bank_account | Номер банковского счета отправителя | INT | NN |
|  | amount | Сумма начисления | INT | NN |
| Отзыв | review_id | Уникальный идентификатор отзыва | DATE | PK |
|  | client_id | Уникальный идентификатор клиента | INT | NN |
|  | employee_id | Уникальный идентификатор сотрудника | INT | NN |
|  | content | Содержание отзыва | VARCHAR(255) | NN |
|  | date | Дата отзыва | INT | NN |
| Запись | appointment_id | Уникальный идентификатор записи | INT | PK |
|  | service_id | Уникальный идентификатор услуги | INT | NN |
|  | client_id | Уникальный идентификатор клиента | INT | NN |
|  | employee_id | Уникальный идентификатор сотрудника | INT | NN |
|  | review_id | Уникальный идентификатор отзыва | INT | NN |
|  | accrual_id | Уникальный идентификатор начисления | INT | NN |
|  | completion_status | Статус выполнения | ENUM | NN |
| Расписание | slot_id | Уникальный идентификатор слота | INT | PK |
|  | employee_id | Уникальный идентификатор сотрудника | INT | NN |
|  | client_id | Уникальный идентификатор клиента | INT | NN |
|  | date | Дата | DATE | NN |
|  | start_time | Время начала | TIME | NN |
|  | end_time | Время окончания | TIME | NN |
|  | slot_status | Статус слота(Свободен/Забронирован) | ENUM | NN |