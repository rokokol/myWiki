---
tags:
  - "#y2025"
  - дискретка
  - учеба
created: 2025-04-18
aliases: 
icon: LiBinary
---
# Лекции по дискретной математике
> Грубо говоря, эти лекции у нас, как таковые, отсутствуют. Поэтому я нашел интересный плейлист, который и собираюсь изучить — мне нравится сам предмет

```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Конспекты/Дискретная математика"
WHERE contains(file.tags, "конспекты")
SORT file.cday DESC
```