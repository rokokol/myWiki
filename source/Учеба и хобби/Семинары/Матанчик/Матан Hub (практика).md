---
icon: LiUnderline
tags:
  - "#y2025"
  - матан
created: 2025-04-18
aliases: 
---
# Семинары по матану
> [!quote] Носкова Евгения Александровна
> За все домашки дают по 1б, $24\geq$ баллов = автомат

---

Семинары:
```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Семинары/Матанчик"
WHERE contains(file.tags, "семинары")
SORT file.cday DESC
```