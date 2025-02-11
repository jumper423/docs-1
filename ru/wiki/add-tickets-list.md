# Вставить ссылки на задачи {{ tracker-name }}

Пользователи [{{ tracker-full-name }}]({{ link-tracker }}) могут размещать на страницах {{ wiki-name }} ссылки на отдельные задачи или списки задач.


## Ссылки на задачи {#tasks}

Чтобы добавить ссылку на задачу, укажите в тексте ее ключ.

Пример:

Разметка | Результат
----- | -----
``` Ошибку устраняем в задаче TEST-123 ``` | ![](../_assets/wiki/tracker-magic-link.png)


## Список задач {#list}

С помощью [динамического действия `not_var{{tasks}}`](actions/objects.md#section_ad2_fkg_1db) вы можете разместить на странице автоматически сформированный список задач. Например:

```
{{tasks url="адрес фильтра или очереди"}}
```

## Список задач с параметрами {#tasks-vars}

С помощью динамических таблиц вы можете разместить на странице список задач и их основные параметры:

1. [Создайте](create-grid.md) динамическую таблицу.

1. Создайте столбец с типом данных **Задача в Трекере**.

1. Добавьте необходимое количество строк и перечислите в них ключи задач.

1. Создайте дополнительные столбцы. В качестве типа данных укажите нужные параметры задачи. Например, **Заголовок**, **Автор** или **Тип** задачи.

1. Сохраните таблицу.

В результате столбцы с параметрами задач заполнятся автоматически. Полученную таблицу можно [разместить на вики-странице](add-grid.md).

Пример:
![](../_assets/wiki/tickets-grid-example.png)