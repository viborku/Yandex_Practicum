## Рекомендация тарифов
В нашем распоряжении данные о поведении клиентов, которые уже перешли на эти тарифы (из проекта курса «Статистический анализ данных»). Нужно построить модель для задачи классификации, которая выберет подходящий тариф. Предобработка данных не понадобится.

Необходимо построить модель с максимально большим значением accuracy. //Нужно довести долю правильных ответов по крайней мере до 0.75. Проверить accuracy на тестовой выборке.

## Вывод
Получены следующие результаты исследования по рассмотренным вариантам.

df = df, size=0.20 (разбивка 80-10-10)
DecisionTreeClassifier Лушие: Depth 6 Accuracy 0.7975077881619937 RandomForestClassifier Лушие: Estimator 20 Accuracy 0.8068535825545171 LogisticRegression Accuracy = 0.7663551401869159

При нашем выборе параметров лучший реультат показывает RandomForestClassifier: Estimator 20 Accuracy 0.8068535825545171

Худший: LogisticRegression Accuracy = 0.7663551401869159

Тестовая выборка: Accuracy = 0.7701863354037267 Ошибок: 160.0 из 3214 - 4.98 %

df = df, size=0.40 (разбивка 60-20-20)
DecisionTreeClassifier Лушие: Depth 3 Accuracy 0.7853810264385692 RandomForestClassifier Лушие: Estimator 50 Accuracy 0.7916018662519441 LogisticRegression Accuracy = 0.7107309486780715

При нашем выборе параметров лучший реультат показывает RandomForestClassifier Лушие: Estimator 50 Accuracy 0.7916018662519441

Худший: LogisticRegression Accuracy = 0.7107309486780715

Тестовая выборка: Accuracy = 0.7822706065318819 Ошибок: 298.0 из 3214 - 9.27 %

df = df_min, size=0.20 (разбивка 80-10-10)
DecisionTreeClassifier Лушие: Depth 4 Accuracy 0.794392523364486 RandomForestClassifier Лушие: Estimator 10 Accuracy 0.8006230529595015 LogisticRegression Accuracy = 0.7663551401869159

При нашем выборе параметров лучший реультат показывает RandomForestClassifier Лушие: Estimator 10 Accuracy 0.8006230529595015

Худший: LogisticRegression Accuracy = 0.7663551401869159

Тестовая выборка: Accuracy = 0.7919254658385093 Ошибок: 155.0 из 3214 - 4.82 %

df = df_min, size=0.40 (разбивка 60-20-20)
DecisionTreeClassifier Лушие: Depth 4 Accuracy 0.7884914463452566 RandomForestClassifier Лушие: Estimator 20 Accuracy 0.7822706065318819 LogisticRegression Accuracy = 0.7076205287713841

При нашем выборе параметров лучший реультат показывает DecisionTreeClassifier Лушие: Depth 4 Accuracy 0.7884914463452566

Худший: LogisticRegression Accuracy = 0.7076205287713841

Тестовая выборка: Accuracy = 0.7776049766718507 Ошибок: 302.0 из 3214 - 9.4 %

Таким образом, лучший результат показывает модель (df_min, size=0.20 (разбивка 80-10-10) RandomForestClassifier Лушие: Estimator 10 Accuracy 0.8006230529595015

Худший: LogisticRegression Accuracy = 0.7663551401869159

Тестовая выборка: Accuracy = 0.7919254658385093 Ошибок: 155.0 из 3214 - 4.82 %
