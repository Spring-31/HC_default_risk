# Прогнозирование вероятности дефолта клиентов

Выпускная квалификационная работа по курсу «Data Science» в Центре дополнительного образования МГТУ им. Н.Э. Баумана по теме: "Прогнозирование вероятности дефолта клиентов"

## Цели и задачи проекта
Целью данной работы является обучение моделей для прогнозирования вероятности дефолта заемщика по кредитам на основании данных, представленных банком Home Credit для соревнования на платформе Kaggle (https://www.kaggle.com/competitions/home-credit-default-risk)

Для достижения целей были сформулированы и решены следующие задачи:

1) Изучены теоретические основы и методы предобработки данных и обучения моделей классификации

2) Выполнен разведочный анализ данных

3) Проведена предобработка данных, включающая в себя добавление агрегированных показателей, анализ и устранение аномалий и выбросов, заполнение пропусков и стандартизацию данных

4) Обучено нескольких моделей для прогноза вероятности дефолта клиента. При построении модели было 30% данных оставлено на тестирование модели, на остальных происходило обучение моделей. 

5) Качество моделей улучшено методом поиска оптимальных гиперпараметров по сетке параметров, а также методом ресамблинга обучающего датасета для устранения несбалансированности данных

6) Обучена полносвязная нейронная сеть

7) Проведена оценка качества обученных моделей на тренировочном и тестовом датасете, сравнение показателей с базовой моделью

8) Создан репозиторий в GitHub и размещен код исследования.

9) Оформлен данный файл README

## Структура репозитория

папка _notebooks_ содержит в себе Jupyter notebooks для разведочного анализа данных, предобработки и обучения моделей  

папка _output_ содержит:
- показатели качества обученных моделей
- результат процедуры отбора наиболее значимых переменных

папка _model_ содержит файлы с предобученной моделью в формате txt и pickle (методы lightgbm.booster_.save_model и pickle.dump соответственно)

в корне размещена документация по исследованию:  
- Постановка задачи прогнозирования вероятности дефолта
- Пояснительная записка прогнозирование вероятности дефолта 
- Презентация "Прогнозирование вероятности дефолта"

requirements.txt - файл с версиями библиотек
Исходные данные не отгружены в репозиторий по причине их размера (более 2Гб). Данные доступны по ссылке https://www.kaggle.com/competitions/home-credit-default-risk 

## Next steps
Дальнейшие шаги по улучшению качества модели:
-  Более тонкую настройку стандартизации непрерывных переменных
-  Снижение размерности, сокращение признаков в выборке, например методом главных компонент (PCA)
-  Подбор гиперпараметров (невозможен в текущем исследовании из-за большого количества признаков)
-  Обучение деревьев на случайных подвыборках (bagging и выбор признаков)
-  Стекинг нескольких ансамблей

Разработка приложение и интеграция обученной модели в приложение

## Автор

Щекина Татьяна Сергеевна
