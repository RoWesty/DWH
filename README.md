# Логическая модель DWH

## Список всех сущностей

### Raw Слой
1. Информация о продажах
1. Личный кабинет покупателя
1. Промо-акции

### Core Слой
2. Товар
 > Связанные сущности
 - Бренд
 - Модель
 - Категории
2. Промо-акции
 > Связанные сущности
 - Время проведения
2. Покупатель
 > Связанные сущности
 - Личный кабинет
 - Продажи

 ## Связи Core слоя
 3. Бренд
  - Бренд - Товар 1 ко многим
  > 1 Бренд выпускает много товаров
3. Модель
  - Модель - Товар 1 ко многим
  > 1 Модель может быть у нескольких товаров
3. Категории
  - Категории - Товар 1 ко многим
  > У нескольких товаров может быть 1 категория
3. Товар
  - Товар - Продажи 1 ко многим
  > 1 товар может продаваться несколько раз
  - Товар - Промо-акции 1 ко многим
  > У одного товара может быть несколько промо-акции в разное время
3. Время проведения
 - Время проведения - Промо-акции 1 к 1
 > У одной промо-акции, 1 время её проведения
3. Покупатель
 - Покупатель - Продажи 1 ко многим
 > 1 Покупатель может купить много товаров
 - Покупатель - личный кабинет 1 ко многим
 > У 1 покупателя может быть несколько личных кабинетов
