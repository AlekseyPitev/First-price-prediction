# First-price-prediction

Задача: Это задача регрессии на предсказание цен на недвижимость в Мельбурне. На основе датасета с рядом признаков и ценой необходимо построить модель предсказания цены. Затем применить модель на тестовых данных с неизвестной ценой. Платформа Kaggle проверяет точность предсказания, метрикой оценки здесь является MAPE (mean absolute Percentage error).  
Стек: python, библиотеки pandas, catboost, phik  
Процесс: Загружается датафрейм с контрольными данными, проводится EDA. Заполняются некоторые пропущенные данные местоположения, которые можно определить точно, по известным признакам и данным с аналогичными значениями известных признаков. Проводится оценка влияния признаков на цену по Фику и на основе корреляционной матрицы. В качестве регрессионной модели используется CatBoost, настраиваются параметры модели, после чего обучаем её на контрольных данных. Загружается в датафрейм файл с данными для тестирования модели. Аналогично заполняются некоторые пропущенные значения в признаках местоположения. Модель применятся, результат с предсказанными ценами выгружается в csv-файл для дальнейшей оценки прогнозирования на Kaggle.  
Результат: Модель показала неплохой результат, с значением MAPE 14.43. В частности, в октябре 2023г позиция в рейтинге была 29 из 108, в настоящее время (февраль 2024) - 37 из 127 (модель не улучшалась). [Ссылка на соревнование на Kaggle](https://www.kaggle.com/competitions/leopard-challenge-regression/overview)

price prediction for Leopard Challenge
This is a regression task for predicting real estate prices in Melbourne. The model's prediction is evaluated here using MAPE (mean absolute percentage error). Using pandas, catboost, and phik, a dataset analysis was conducted, some missing data was filled in, an optimal set of parameters was selected, and price prediction was performed. The position in the rating is 29/108 (2023.10).

https://www.kaggle.com/competitions/leopard-challenge-regression/overview
