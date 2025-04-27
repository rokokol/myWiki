---
icon: LiAtom
tags:
  - "#y2025"
  - умф
  - учеба
  - кфу
created: 2025-04-11
aliases: 
---

# Лекции по уравнениям математической физике
> Курс читается по книгам *Тихонова* и *Самарского* "Уравнения Математической Физики"

---

```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Конспекты/Уравнения математической физики"
WHERE contains(file.tags, "кфу") AND
contains(file.tags, "конспекты")
SORT file.cday DESC
```
