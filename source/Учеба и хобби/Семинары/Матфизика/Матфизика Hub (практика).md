---
icon: LiAtom
tags:
  - "#y2025"
  - "#умф"
created: 2025-04-18
aliases: 
---

# Семинары по уравнениям математической физики
> [!quote] Глазырина Младшая
> На кр будут задачи из дз

---
```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Семинары/Матфизика"
WHERE contains(file.tags, "семинары")
SORT file.cday DESC
```
