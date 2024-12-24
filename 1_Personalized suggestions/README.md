# Прогнозирование прибыли от нефтяных скважин
<h1>Содержание<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Прогнозирование-прибыли-от-нефтяных-скважин" data-toc-modified-id="Прогнозирование-прибыли-от-нефтяных-скважин-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Прогнозирование прибыли от нефтяных скважин</a></span><ul class="toc-item"><li><span><a href="#Описание-проекта" data-toc-modified-id="Описание-проекта-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Описание проекта</a></span></li><li><span><a href="#Описание-данных" data-toc-modified-id="Описание-данных-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Описание данных</a></span></li><li><span><a href="#Условия-задачи" data-toc-modified-id="Условия-задачи-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Условия задачи</a></span></li><li><span><a href="#Вывод" data-toc-modified-id="Вывод-1.4"><span class="toc-item-num">1.4&nbsp;&nbsp;</span>Вывод</a></span></li></ul></li></ul></div>









## Описание проекта
К вам обратился фермер, владелец молочного хозяйства «Вольный луг». Он хочет купить бурёнок, чтобы расширить поголовье стада коров. Для этого он заключил выгодный контракт с ассоциацией пастбищ «ЭкоФерма».
Условия позволяют фермеру очень тщательно отобрать коров. Он определяет качество молока по строгой методике, и при этом ему нужно выполнять свой план развития молочного хозяйства. Фермер хочет, чтобы каждая бурёнка давала не менее 6000 килограммов молока в год, а её надой был вкусным — строго по его критериям, ничуть не хуже.
Поэтому он просит вас разработать модель машинного обучения, которая поможет ему управлять рисками и принимать объективное решение о покупке. «ЭкоФерма» готова предоставить подробные данные о своих коровах.


## Описание данных


Вы можете их скачать, нажав на название каждого.
1.	Файл ferma_main.csv содержит данные о стаде фермера на текущий момент. Описание данных: 
-	id — уникальный идентификатор коровы.
-	Удой, кг — масса молока, которую корова даёт в год (в килограммах).
-	ЭКЕ (Энергетическая кормовая единица) — показатель питательности корма коровы.
-	Сырой протеин, г — содержание сырого протеина в корме (в граммах).
-	СПО (Сахаро-протеиновое соотношение) — отношение сахара к протеину в корме коровы.
-	Порода — порода коровы.
-	Тип пастбища — ландшафт лугов, на которых паслась корова.
-	порода папы_быка — порода папы коровы.
-	Жирность,% — содержание жиров в молоке (в процентах).
-	Белок,% — содержание белков в молоке (в процентах).
-	Вкус молока — оценка вкуса по личным критериям фермера, бинарный признак (вкусно, не вкусно).
-	Возраст — возраст коровы, бинарный признак (менее_2_лет, более_2_лет).



## Условия задачи
Вам нужно создать две прогнозные модели для отбора бурёнок в поголовье:
- Первая будет прогнозировать возможный удой коровы (целевой признак Удой);
- Вторая — рассчитывать вероятность получить вкусное молоко от коровы (целевой признак Вкус молока).
С помощью модели нужно отобрать коров по двум критериям:
- средний удой за год — не менее 6000 килограммов;
- молоко должно быть вкусным.

## Вывод

- Нулевой регион:
    - Доверительный интервал: (-110 929 096.14, 891 087 236.3)
    - Точка безубыточности: 111.(1)
    - Средняя прибыль в нулевом регионе: 381 840 608.64
    - Риски: 6.7 %
- Второй регион: 
    - Доверительный интервал: (-142 559 672.52, 900 660 974.77)
    - Точка безубыточности: 111.(1)
    - Средняя прибыль с одной скважины во втором регионе: 382 973 380.22
    - Риски: 7 %
        
по условию рисков не подходит ни один из регионов. Если же выбирать из наименее рискованных, то наиболее подходящим будет нулевой регион. Но также можно заметить, что по сравнению со вторым регионом у него средняя прибыль меньше, в тоже время у второго региона на 0,3% выше риски.  