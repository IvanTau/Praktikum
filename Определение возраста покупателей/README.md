# Определение возраста покупателей
Сетевой супермаркет внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:
- Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
- Контролировать добросовестность кассиров при продаже алкоголя.
Построена модель, которая по фотографии определит приблизительный возраст человека.

## Статус проекта
Завершен

## Общий вывод
Был проведен анализ датасета и дообучена модель ResNet50, предсказывающая возраст людей. В среднем модель ошибается на 5.2 года. Теперь эту модель можно использовать для определения возраста покупателей.

## Описание данных

Датасет AppaReal на 7,591 фотографий с лицами людей.
