# Прогнозирование количество заказов такси на следующий час
<h1>Содержание<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Прогнозирование-количество-заказов-такси-на-следующий-час" data-toc-modified-id="Прогнозирование-количество-заказов-такси-на-следующий-час"><span class="toc-item-num">1&nbsp;&nbsp;</span>Прогнозирование количество заказов такси на следующий час</a></span><ul class="toc-item"><li><span><a href="#Описание-проекта" data-toc-modified-id="Описание-проекта-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Описание проекта</a></span></li><li><span><a href="#Описание-данных" data-toc-modified-id="Описание-данных-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Описание данных</a></span></li><li><span><a href="#Условия-задачи" data-toc-modified-id="Условия-задачи-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Условия задачи</a></span></li><li><span><a href="#Вывод" data-toc-modified-id="Вывод-1.4"><span class="toc-item-num">1.4&nbsp;&nbsp;</span>Вывод</a></span></li></ul></li></ul></div>









## Описание проекта
Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. Основная задача проекта — спрогнозировать количество заказов такси на следующий час, чтобы обеспечить привлечение большего числа водителей в период пиковой нагрузки. Для успешного выполнения задачи необходимо построить модель, предсказания которой на тестовой выборке будут иметь значение метрики RMSE не больше 48.


## Описание данных


Основной столбец данных — num_orders


## Условия задачи
- Значение метрики RMSE на тестовой выборке должно быть не больше 48.

## Вывод

В ходе работы над исследованием была обучена, выбрана и протестирована лучшая модель машинного обучения CatBoostRegressor, прогнозирующая количество заказов такси в следующий час. Финальное качество модели на тестовой выборке: RMSE = 36.80958977673447