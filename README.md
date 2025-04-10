# Мастерская 2 Проект "Маркетинг"
Интернет-магазин собирает историю покупателей, проводит рассылки предложений и планирует будущие продажи. Для оптимизации процессов надо выделить пользователей, которые готовы совершить покупку в ближайшее время.    

## Цель исследования:   
Построить модель машинного обучения, которая для каждого клиента сможет предсказать вероятность покупки в интернет-магазине в течение 90 дней, проверить качество модели метрикой ROC-AUC.    

##  План проекта: 
Шаг 1. Подготовка данных    
Загрузка и предобработка данных: обработка пропусков, дубликатов, аномалий, проверка типов данных;    
Объединение таблиц, разработка новых признаков;      
Исследовательский анализ данных: исследование и корреляционный анализ признаков;          
Подготовка выборок для обучения моделей;      
Вывод по разделу   

Шаг 2. Обучение моделей    
Создание пайплайна, обучение и получение предсказаний следующих моделей: LogisticRegression, KNeighborsClassifier и CatBoostRegressor;   
Выбор лучшей модели;   
Вывод по разделу   

Шаг 3. Анализ моделей   
Получение предсказания, определение качества лучшей модели (метрикой ROC-AUC), анализ ошибок;   
Вывод по разделу   

Шаг 4. Общий вывод и рекомендации   

##  Описание изначальных данных:   
1. apparel-purchases (история покупок):   
● client_id - идентификатор пользователя;   
● quantity - количество товаров в заказе;   
● price - цена товара;    
● category_ids - вложенные категории, к которым относится товар;   
● date - дата покупки;   
● message_id - идентификатор сообщения из рассылки;   

2. apparel-messages (история рекламных рассылок):   
● bulk_campaign_id - идентификатор рекламной кампании;   
● client_id - идентификатор пользователя;   
● message_id - идентификатор сообщений;   
● event - тип действия;  
● channel - канал рассылки;   
● date - дата рассылки;   
● created_at - точное время создания сообщения;   

3. apparel-target_binary (совершит ли клиент покупку в течение следующих 90 дней):   
● client_id - идентификатор пользователя;   
● target - целевой признак.   
