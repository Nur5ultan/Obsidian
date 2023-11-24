#dataview #column_file

Что бы переименовать первый столбец в Dataview используем следующий код

```
TABLE WITHOUT ID
  file.link AS "Some other name",
  foo AS "Foo"
FROM #bar
```

Основываясь на комментарии [@robmiller](https://github.com/robmiller), на случай, если это кому-то еще пригодится, вот фрагмент, чтобы сохранить ссылку на файл, но изменить отображаемый текст на другой - значения другого столбца (`title`):

```
TABLE WITHOUT ID
  link(file.link, title) AS "Title",
  foo AS "Foo"
FROM #bar
```

Или [неявное поле](https://blacksmithgu.github.io/obsidian-dataview/data-annotation/#implicit-fields):

```
TABLE WITHOUT ID
  link(file.link, file.path) AS "File Path",
  foo AS "Foo"
FROM #bar
```