---
editable: false
---

# DATEADD

_Функции даты и времени_

#### Синтаксис {#syntax}


```
DATEADD( datetime, unit, number )
```

#### Описание {#description}
Возвращает дату, полученную в результате добавления `unit` в количестве `number` к указанной дате `datetime`.

Аргумент `number` задается целым числом. Может принимать отрицательные значения.
Аргумент `unit` принимает следующие значения:
- `"year"` — год,
- `"month"` — месяц,
- `"day"` — день,
- `"hour"` — час,
- `"minute"` — минута,
- `"second"` — секунда.

**Типы аргументов:**
- `datetime` — `Дата | Дата и время`
- `unit` — `Строка`
- `number` — `Целое число`


**Возвращаемый тип**: Совпадает с типом аргументов (`datetime`)

{% note info %}

Значения аргументов (`unit`) должны быть константами.

{% endnote %}

{% note info %}

Для всех источников кроме `Материализованный датасет`, `ClickHouse` аргумент `number` принимает только константые значения.

{% endnote %}


#### Примеры {#examples}

```
DATEADD(#2018-01-12#, "day", 6) = #2018-01-18#
```

```
DATEADD(#2018-01-12#, "month", 6) = #2018-07-12#
```

```
DATEADD(#2018-01-12#, "year", 6) = #2024-01-12#
```

```
DATEADD(#2018-01-12 01:02:03#, "second", 6) = #2018-01-12 01:02:09#
```

```
DATEADD(#2018-01-12 01:02:03#, "minute", 6) = #2018-01-12 01:08:03#
```

```
DATEADD(#2018-01-12 01:02:03#, "hour", 6) = #2018-01-12 07:02:03#
```

```
DATEADD(#2018-01-12 01:02:03#, "day", 6) = #2018-01-18 01:02:03#
```

```
DATEADD(#2018-01-12 01:02:03#, "month", 6) = #2018-07-12 01:02:03#
```

```
DATEADD(#2018-01-12 01:02:03#, "year", 6) = #2024-01-12 01:02:03#
```


#### Поддержка источников данных {#data-source-support}

`Материализованный датасет`, `ClickHouse 1.1`, `Microsoft SQL Server 2017 (14.0)`, `MySQL 5.6`, `PostgreSQL 9.3`.