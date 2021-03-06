# Восстановление золота из руды

Компания разрабатывает решения для эффективной работы золотодобывающей отрасли.
Построена модель, предсказывающая коэффициент восстановления золота из золотосодержащей руды. Проанализированы данные с параметрами добычи и очистки.
Построена и обучена модель, помогающая оптимизировать производство на двух этапах обработки руды, чтобы не запускать предприятие с убыточными характеристиками.

## Статус проекта
Завершен

## Общий вывод
Лучшей моделью для предсказания этапа флотации оказался Случайный лес глубиной 7 на 70 деревьев. Она превзошла случайную модель на 1 пункт.

Лучшей моделью для финальной очистки оказался так же Случайный лес, но глубина уменьшилась до 5. Эта модель превзошла случайную на 2 пункта.

Итоговое sMAPE Случайного леса равно 5.41 против 7.14 у случайной модели.

## Технологический процесс
- Rougher feed — исходное сырье
- Rougher additions (или reagent additions) — флотационные реагенты: Xanthate, Sulphate, Depressant
- Xanthate **— ксантогенат (промотер, или активатор флотации);
- Sulphate — сульфат (на данном производстве сульфид натрия);
- Depressant — депрессант (силикат натрия).
- Rougher process (англ. «грубый процесс») — флотация
- Rougher tails — отвальные хвосты
- Float banks — флотационная установка
- Cleaner process — очистка
- Rougher Au — черновой концентрат золота
- Final Au — финальный концентрат золота  


## Параметры этапов
air amount — объём воздуха
fluid levels — уровень жидкости
feed size — размер гранул сырья
feed rate — скорость подачи  


## Наименование признаков

Наименование признаков формируется по следующему принципу:  

__[этап].[тип_параметра].[название_параметра]__  

Пример: rougher.input.feed_ag

### Возможные значения для блока [этап]
- rougher — флотация
- primary_cleaner — первичная очистка
- secondary_cleaner — вторичная очистка
- final — финальные характеристики  


### Возможные значения для блока [тип_параметра]
- input — параметры сырья
- output — параметры продукта
- state — параметры, характеризующие текущее состояние этапа
- calculation — расчётные характеристики

### Целевые признаки
- эффективность обогащения чернового концентрата rougher.output.recovery;
- эффективность обогащения финального концентрата final.output.recovery.
