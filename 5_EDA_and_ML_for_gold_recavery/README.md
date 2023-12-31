# Восстановление золота из руды
|Сферы деятельности|Направление деятельности|Навыки и инструменты|Ключевые слова проекта|Статус проекта| 
|:-----------------|:-----------------------|:-------------------|:---------------------|:-------------:|
|Промышленность|Машинное обучение, Аналитик(универсал)|*Python, Pandas, Matplotlib, Scikit-learn, NumPy*, исследовательский анализ данных|анализ данных, регрессия, кастомные метрики|Завершен|

**Постановка задачи:**

Подготовьте прототип модели машинного обучения для «Цифры»(https://www.zyfra.com/ru/). Компания разрабатывает решения для эффективной работы промышленных предприятий.

Модель должна предсказать коэффициент восстановления золота из золотосодержащей руды. Используйте данные с параметрами добычи и очистки. 

Модель поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.

Вам нужно:

1. Подготовить данные;
2. Провести исследовательский анализ данных;
3. Построить и обучить модель.

Чтобы выполнить проект, обращайтесь к библиотекам *pandas*, *matplotlib* и *sklearn.* Вам поможет их документация.

**Цель исследования:** 
1. Анализ процесса обработки золота из руды, выбор модели для выбора оптимизации процесса обработки с помощью машинного обучения.

**Задачи исследования:**
1. Подготовить и разделить 2 набора данных(обучающие и тестовые) на несколько выборок(флотация, весь процесс, целевые признаки, факторы);
2. Проанализировать концентрации металлов и их распределение на этапах обработки;
3. Оценить разницу распределения размера гранул сырья;
4. Обучение и проверка модели.

**Объектом исследования** является данные процесса очистки золотой руды.

**Предметом исследования** является комплекс методик машинного обучения и инструментов связанных с МО.

**Ход выполнения**
1. Импортировать все необходимые библиотеки
2. Загрузить данные из трех файлов
3. Проанализировать общую информацию о качестве и структуре данных, предобработать данные
4. Наглядно продемонстрировать распределение концентрации металлов на разныхх стадиях обработки
5. Подобрать оптимальную модель на тренировочном наборе данных с помощью кросс-валидации
6. Проверить модель на тестовой выборке
7. Сделать выводы и рекомендации для дальнейшего исследования

**Описание данных**
Есть 3 набора данных: обучающий, тестовый и сборный. Каждая строчка это характеристики всего процесса (всех этапов) обработки поступившего сырья в определенное время. 

Известно:
- `date` — время загрузки сырья;
- большое количество характеристик процесса обработки(например, входные и выходные концентраты металлов, настройки оборудования);

Целевые признаки
- `rougher.output.recovery` — эффективность флотации;
- `final.output.recovery` - эффективность финальная.
