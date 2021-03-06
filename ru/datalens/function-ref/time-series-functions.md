---
editable: false
---

# Функции для работы с временными рядами
Эти функции позволяют получать значения показателя, отнесенного к конкретным дате и времени. Дата и время задаются либо точными значениями, либо в виде смещения вдоль заданной временной оси.

В некоторой степени эти функции схожи с оконной [LAG](LAG.md).

Основное отличие — `LAG` не учитывает значения измерений и использует смещение, заданное в виде количества строк.

Функции временных рядов работают с конкретными значениями или смещениями, заданными во временных единицах (дни, часы или секунды). За счет этого они становятся чувствительными к пропущенным значениям в данных. В результате, формула `AGO(SUM([Sales]), [Date], "year")` вернет `NULL`, если отсутствуют данные на ту же дату за предыдущий год.


## [AGO](AGO.md)

**Синтаксис:**`AGO( measure, date_dimension [ , unit [ , number ] ] )`

Вычисляет `measure` для даты/времени с указанным смещением.
Аргумент `date_dimension` задает измерение, вдоль которого делается смещение.
Аргумент `number` задается целым числом. Может принимать отрицательные значения.
Аргумент `unit` принимает следующие значения:
- `"year"` — год;
- `"month"` — месяц;
- `"day"` — день;
- `"hour"` — час;
- `"minute"` — минута;
- `"second"` — секунда.

Возможен вариант использования `AGO( measure, date_dimension, number )`. В этом случае аргумент `unit` — количество дней.

Обратите внимание, что это не оконная функция и она не поддерживает такие параметры, как `BEFORE FILTER BY`.

См. также [AT_DATE](AT_DATE.md), [LAG](LAG.md).



## [AT_DATE](AT_DATE.md)

**Синтаксис:**`AT_DATE( measure, date_dimension, date_expr )`

Вычисляет `measure` для даты/времени, заданных выражением `date_expr`.
Аргумент `date_dimension` задает измерение, вдоль которого делается смещение.

См. также [AGO](AGO.md), [LAG](LAG.md).


