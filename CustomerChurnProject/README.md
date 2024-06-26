# Прогнозирование оттока клиентов.
# Описание проекта:
Оператор связи «ТелеДом» хочет бороться с оттоком клиентов. Для этого его сотрудники начнут предлагать промокоды и специальные условия всем, кто планирует отказаться от услуг связи. Чтобы заранее находить таких пользователей, «ТелеДому» нужна модель, которая будет предсказывать, разорвёт ли абонент договор. Команда оператора собрала персональные данные о некоторых клиентах, информацию об их тарифах и услугах. Наша задача — обучить на этих данных модель для прогноза оттока клиентов. В качестве метрики будет использоваться ROC-AUC, его значение должно быть больше 85.


# Вывод.
В данной работе был проведен подробный исследовательский анализ. Для данной задачи обучили три модели классификации - LogisticRegression, RandomForestClassifier и CatBoostClassifier. В качестве метрики использовали метрику ROC-AUC.<br>
1) LogisticRegression. Метрика ROC-AUC лучшей модели на тренировочной выборке: 0.7590407683084738. Метрика оказалась слишком низкой.<br>
2) RandomForestClassifier. Наблюдаем прирост в качестве по сравнению с логистической регрессией, "ROC-AUC" - 0.8201479645582989, но это также ниже требуемого.<br>
3) CatBoostClassifier. CatBoostClassifier добился требуемой метрики ROC-AUC - 0.856141795061295 на тренировочной выборке. Именно эту модель выбрали для прогноза на тестовых данных.<br>
4) Метрика ROC-AUC на тестовой выборке для CatBoostClassifier: 0.9019968187935886, что полностью удовлетваряет условию задачи ROC-AUC > 85.
