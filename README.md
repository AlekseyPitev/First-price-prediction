# First-price-prediction

**Задача**: Это задача регрессии на предсказание цен на недвижимость в Мельбурне. На основе датасета с рядом признаков и ценой необходимо построить модель предсказания цены. Затем применить модель на тестовых данных с неизвестной ценой. Платформа Kaggle проверяет точность предсказания, метрикой оценки здесь является MAPE (mean absolute Percentage error).  

**Стек**: python, библиотеки pandas, catboost, phik, matplotlib  

**Процесс**: Загрузил датафрейм с контрольными данными и провёл EDA. Заполнил некоторые пропущенные данные местоположения, которые можно определить точно, по известным признакам и данным с аналогичными значениями известных признаков. Затем провёл оценку влияния признаков на цену по Фику и на основе корреляционной матрицы. В качестве регрессионной модели использовал CatBoost, настроил параметры модели, после чего обучил её на контрольных данных. Загрузил в датафрейм файл с данными для тестирования модели. Аналогично заполнил некоторые пропущенные значения в признаках местоположения. Применил обученную модель, результат с предсказанными ценами выгрузил в csv-файл для дальнейшей оценки прогнозирования на Kaggle.  

**Результат**: Модель показала неплохой результат, с значением MAPE 14.43. В частности, в октябре 2023г позиция в рейтинге была 29 из 108, в настоящее время (февраль 2024) - 37 из 127 (модель не улучшалась). [Ссылка на соревнование на Kaggle](https://www.kaggle.com/competitions/leopard-challenge-regression/overview)

Price prediction for Leopard Challenge
This is a regression task for predicting real estate prices in Melbourne. The model's prediction is evaluated here using MAPE (mean absolute percentage error). Using pandas, catboost, and phik, a dataset analysis was conducted, some missing data was filled in, an optimal set of parameters was selected, and price prediction was performed. The position in the rating is 29/108 (2023.10).

https://www.kaggle.com/competitions/leopard-challenge-regression/overview
