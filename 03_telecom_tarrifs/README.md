# Определение выгодного тарифа для телеком компании
## Описание проекта:
Проведен предварительный анализ использования тарифов на выборке клиентов, проанализировано поведение клиентов при использовании услуг оператора и рекомендованы оптимальные наборы услуг для пользователей. Проведена предобработка данных, их анализ. Добавлены недостающие данные, которые необходимы для анализа. Проверены гипотезы о различии выручки абонентов разных тарифов и различии выручки абонентов из Москвы и других регионов при помощи t-критерия Стьюдента.
## Результат:
Выявили статистически значимое различие в выручке двух тарифов. При сравнении средней выручки из Москвы и регионов у нас не нашлось оснований отклонить нулевую гипотезу об их равенстве, так как уровень значимости оказался выше заданного 5%-го значения. Наиболее выгодным тарифом оказался Smart, так как имеет большую долю пользователей, в том числе тех, которые часто совершают доплаты сверх пакета.
## Описание тарифов:
| Услуга | "Smart" | "Ultra"|
|:----|:----|:----------|
|Абонентская плата|550|1950|
|Количество минут|500|3000|
|Количество сообщений|50|1000|
|Объем интернет-трафика|15 гб| 30 гб|
|Минута разговора сверх пакета| 3 р|1 р|
|Сообщение сверх пакета| 3 р|1 р|
|Трафик сверх пакета|200 р|150 р|

## Описание данных:
### Таблица users (информация о пользователях):
- user_id — уникальный идентификатор пользователя
- first_name — имя пользователя
- last_name — фамилия пользователя
- age — возраст пользователя (годы)
- reg_date — дата подключения тарифа (день, месяц, год)
- churn_date — дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных)
- city — город проживания пользователя
- tariff — название тарифного плана

### Таблица calls (информация о звонках):
- id — номер звонка
- call_date — дата звонка
- duration — длительность звонка, мин
- user_id — id пользователя

### Таблица messages (информация о сообщениях):
- id — номер сообщения
- message_date — дата сообщения
- user_id — id пользователя

### Таблица internet (информация об интернет-сессиях):
- id — номер сессии
- mb_used — количество пораченных мегабайт
- session_date — дата сессии
- user_id — id пользователя

### Таблица tariffs (информация о тарифах):
- tariff_name — название тарифа
- p rub_monthly_fee — абонентская плата 
- minutes_included — количество включенных минут разговора 
- messages_included — количество включенных сообщений 
- mb_per_month_included — количество включенных мегабайт
- rub_per_minute — стоимость минуты разговора при превышении лимита
- rub_per_message — стоимость отправки сообщения при превышении лимита
- rub_per_gb — стоимость дополнительного гигабайта при превышении лимита

## Используемые библиотеки:
- pandas
- numpy
- math
- seaborn
- scipy
