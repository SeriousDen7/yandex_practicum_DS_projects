# Определение стоимости автомобилей
|Сферы деятельности|Направление деятельности|Навыки и инструменты|Ключевые слова проекта|Статус проекта| 
|:-----------------|:-----------------------|:-------------------|:---------------------|:-------------:|
|Интернет-сервисы, Интернет-магазины, Бизнес|Машинное обучение|*Python, Pandas, LightGBM*|градиентный бустинг, регрессия|Завершен|

Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. В нашем распоряжении исторические данные: технические характеристики, комплектации и цены автомобилей. Необходимо построить модель для определения стоимости. 

Заказчику важны:

- качество предсказания;
- скорость предсказания;
- время обучения.

**Цель исследования:** 
1. Создание модели машинного обучения предсказания стоимости б/у автомобиля по его характеристикам (важным является точность и скорость модели)

**Задачи исследования:**
1. Предобработать данные
2. Разделить данные на выборки (обучающая и тестовая, признаки и целевой показатель)
3. Проверить модели машинного обучения на данных
4. Сравненить результаты моделей по критериям оценки.

**Объектом исследования** являются данные о стоимости и характеристиках б/у автомобилей.

**Предметом исследования** является комплекс методик машинного обучения и инструментов связанных с МО.

**Ход выполнения**
1. Импортировать все необходимые библиотеки
2. Загрузить данные из файла `/datasets/autos.csv`
3. Проанализировать общую информацию о качестве и структуре данных, предобработать данные
4. Разделить данные на выборки
5. Построить разные модели предсказания цены 
6. Сравнить скорость и точность построенных моделей (Значение метрики RMSE должно быть меньше 2500)
7. Сделать выводы и рекомендации для дальнейшего исследования

**Описание данных**
Есть набор данных `/datasets/autos.csv`, каждая строчка это информация по одной заявке на продажу: стоимость и характеристики автомобиля. 

Признаки
- `DateCrawled` — дата скачивания анкеты из базы
- `VehicleType` — тип автомобильного кузова
- `RegistrationYear` — год регистрации автомобиля
- `Gearbox` — тип коробки передач
- `Power` — мощность (л. с.)
- `Model` — модель автомобиля
- `Kilometer` — пробег (км)
- `RegistrationMonth` — месяц регистрации автомобиля
- `FuelType` — тип топлива
- `Brand` — марка автомобиля
- `Repaired` — была машина в ремонте или нет
- `DateCreated` — дата создания анкеты
- `NumberOfPictures` — количество фотографий автомобиля
- `PostalCode` — почтовый индекс владельца анкеты (пользователя)
- `LastSeen` — дата последней активности пользователя

Целевой признак
- `Price` — цена (евро)
