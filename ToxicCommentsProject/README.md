# Проект для «Викишоп»
Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 

Обучим модель классифицировать комментарии на позитивные и негативные. В нашем распоряжении набор данных с разметкой о токсичности правок.

Требование - построить модель со значением метрики качества *F1* не меньше 0.75. 

**Краткий план выполнения проекта**

1. Загрузить и подготовить данные.
2. Обучить разные модели. 
3. Сделаем выводы.


# Вывод.
В ходе работы были протестированны три модели - LogisticRegression, RandomForestClassifier и LGBMClassifier. Лучшие показатели у LogisticRegression, на тестовых данных метрика F1 составила 0.7569678201157937, что подходит под требования задачи -  F1 не меньше 0.75.
