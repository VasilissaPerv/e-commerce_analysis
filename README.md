# e-commerce_analysis
Анализ покупок в интернет-магазине
### Цель:
Проанализировать данные о пользователях, заказах и товарах за 1,5 года.
### Стэк
pandas, plotly, numpy, datetime, matplotlib, requests
### Этапы работы:
1. Предварительный анализ данных (выявить аномалии, отсутствие данных)
2. Найдено количество пользователей, совершивших покупку только один раз
3. Рассчитано, сколько заказов в месяц в среднем не доставляется по разным причинам. Выведена детализация по причинам
4. Для каждого товара определено, в какой день недели его чаще всего приобретают
5. Рассчитано, сколько у каждого из пользователей в среднем покупок в неделю (по месяцам)
6. Выполнен когортный анализ пользователей
7. Проведён RFM анализ
#### По результатам анализа сформулированы выводы для бизнеса:
- Для заказов со статусом unavailable предположительная причина - отсутствие товара на складе/отсутствие продавца
- Также, был сделан вывод о том, что бОльшую часть заказов отменяют уже после оплаты (483 из 625)
- Опоздавших заказов больше (2202), чем по какой-то причине недоставленных (1316)
- Практически все клиенты (кроме 4х) совершали менее одного заказа в неделю
- По результатам RFM анализа видно, что больше половины клиентов совершали покупку более 6 месяцев назад на сумму менее 200 рублей. При этом, приток новых клиентов только 10% от общего количества. Нужно сделать упор на небольшое количество оставшихся клиентов и активнее работать над привлечением новых.
 ![RFM](https://github.com/VasilissaPerv/e-commerce_analysis/blob/main/RFM.png?raw=true)
#### Выводы по результатам когортного анализа:
- Через 1 месяц возвращается наибольший процент юзеров, для всех случаев, кроме когорты 2017-02
- Дальше показатели разнятся сильнее, когорты с наилучшими показателями на долгой дистанции: 2017-05, 2017-06, 2017-08, в следующие месяцы в целом тоже неплохие показатели, но о них пока мало данных
- Есть предположение, что примерно с 2017-04 магазин ввёл какое-то изменение, которое увеличило retention и он стал более стабильным, так как в первые 4 месяца 2017 года показатели были скачущими, самая неудачная когорта: 2017-02
- В целом можно сказать, что retention кажется очень низким, при самых удачных обстоятельствах 0,5-0,7%
 ![COHORT](https://github.com/VasilissaPerv/e-commerce_analysis/blob/main/cohorts.png?raw=true)
