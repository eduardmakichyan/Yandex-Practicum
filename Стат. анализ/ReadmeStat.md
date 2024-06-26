# Описание проекта:
В нашем распоряжение данные популярного сервиса аренды самокатов GoFast. Данные о некоторых пользователях из нескольких городов, а также об их поездках. Проанализируем данные и проверьте некоторые гипотезы, которые могут помочь бизнесу вырасти:
1.  Важно понять, тратят ли пользователи с подпиской больше времени на поездки? Если да, то пользователи с подпиской могут быть «выгоднее» для компании. 
2. Расстояние одной поездки в 3130 метров — оптимальное с точки зрения износа самоката. Можно ли сказать, что среднее расстояние, которое проезжают пользователи с подпиской за одну поездку, не превышает 3130 метров? 
3. Проверем гипотезу о том, будет ли помесячная выручка от пользователей с подпиской по месяцам выше, чем выручка от пользователей без подписки. 
<br>

# Общий вывод:
В данной работе были выполненны следующие шаги:
1. Знакомство с данными, изучение общей информации о таблицах.
2. Предобработка данных :
 1. Формат записи даты был приведет к "datetime64".
 2. Был добавлен новый столбец с номером месяца.
 3. Проверели есть ли пропуски и дуликаты во всех таблицах. Избавились от явных дубликатов. <br>
 Причины возникновения дубликатов : <br>
1) Технические ошибки с многократной загрузкой одного фрагмента данных.<br>
2) Повторный ввод одной и той же информации в сочетании с отсутствием проверок на существование такой же записи в базе данных.<br>
3. Исследовательский анализ данных. В результате анализа было выявленно , что : <br>
1) Главными городами, по использованию самакатов являются - Пятигорск, Екатеринбург.<br>
2) Большая часть клиентов пользуются самокатами без подписки.<br>
3) Основная масса пользователей это люди в возрасте от 22 до 28 лет.<br>
4) Основное кол-во поездок происходит на росстояние примерно от 2500 до 3100 метров.<br>
5) В основном поездки длятся от 13 до 21 минуты.<br>
4. Объединение данных в одну общую таблицу. Создали две отдельные таблицы из объединенной для двух груп пользователей  .Визуализировали информацию о расстоянии и времени поездок для пользователей обеих категорий. В результате было выявленно , что :<br>
1) Расстояние поездок практически одинаково для обеих груп пользователей.<br>
2) Продолжительност поездок незначительно больше у пользователей с подпиской.<br>
5. Подсчёт выручки. Создали датафрейм с агрегированными данными о поездках на основе общей таблицы: найшли суммарное расстояние, количество поездок и суммарное время для каждого пользователя за каждый месяц. Добавили столбец с помесячной выручкой, которую принёс каждый пользователь.
6. Проверка гипотез:
1) Первая гипотеза: тратят ли пользователи с подпиской больше времени на поездки? - В результате теста можно сделать вывод,что пользователи с подпиской трят больше времени на поездки.
2) Вторая гипотеза: можно ли сказать, что среднее расстояние, которое проезжают пользователи с подпиской за одну поездку, не превышает 3130 метров? -  В результате теста можно сделать вывод, что среднее расстояние, которое проезжают пользователи с подпиской за одну поездку, не превышает 3130 метров.
3) Третья гипотиза : будет ли помесячная выручка от пользователей с подпиской по месяцам выше, чем выручка от пользователей без подписки? - Можно сделать вывовод , что месячная выручка от пользователей с подпиской по месяцам выше, чем выручка от пользователей без подписки. <br>
<br>
Подводя итоги можно сделать вывод о том, что пользователи с подпиской "представляют больший интерес" для компании. На них и стоит сделать акцент при проведении рекламных акций.
