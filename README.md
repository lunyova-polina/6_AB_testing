# Проведение анализа A/B-тестирования
В крупном интернет-магазине, вместе с отделом маркетинга, был подготовлен список гипотез для увеличения выручки.  
Чтобы не ошибиться в выборе гипотезы, нужно их приоритизировать и провести A/B-тесты.
A/B-тестирование позволяет узнать различие между группами или его отсутствие, сравнивая различные метрики.

Цели:
1. подготовить данные к анализу;  
2. приоритизировать гипотезы;  
3. запустить A/B-тест;  
4. проанализировать результаты.   
  
В ходе работы нужно выполнить следующие задачи: 

- Применить фреймворк ICE и RICE для приоритизации гипотез;  
- Построить график кумулятивной выручки и кумулятивного среднего чекапо группам;
- Построить график относительного изменения кумулятивного среднего чека группы B к группе A;
- Построить график кумулятивной конверсии по группам;
- Построить график относительного изменения кумулятивной конверсии группы B к группе A;
- Построить точечные графики количества и стоимостей заказов по пользователям;
- Посчитать 95-й и 99-й перцентили количества и стоимости заказов на пользователя. Выбрать границу для определения аномальных пользователей;
- Посчитать статистическую значимость различий в конверсии между группами по «сырым» и «очищенным» данным;
- Посчитать статистическую значимость различий в среднем чеке заказа между группами по «сырым» и «очищенным» данным;
- Принять решение по результатам теста. 
## Описание данных   
  
Данные для первой части  
Файл /datasets/hypothesis.csv  
- `Hypothesis` — краткое описание гипотезы;  
- `Reach` — охват пользователей по 10-балльной шкале;  
- `Impact` — влияние на пользователей по 10-балльной шкале;  
- `Confidence` — уверенность в гипотезе по 10-балльной шкале;  
- `Efforts` — затраты ресурсов на проверку гипотезы по 10-балльной шкале. Чем больше значение Efforts, тем дороже проверка гипотезы.  

Данные для второй части
Файл /datasets/orders.csv
- `transactionId` — идентификатор заказа;
- `visitorId` — идентификатор пользователя, совершившего заказ;
- `date` — дата, когда был совершён заказ;
- `revenue` — выручка заказа;
- `group` — группа A/B-теста, в которую попал заказ.

Файл /datasets/visitors.csv
- `date` — дата;
- `group` — группа A/B-теста;
- `visitors` — количество пользователей в указанную дату в указанной группе A/B-теста
