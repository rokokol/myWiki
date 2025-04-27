---
icon: LiGitGraph
tags:
  - "#y2025"
  - дискретка
created: 2025-04-18
aliases: 
---

# Семинары по дискретной математике
> [!quote] Алия Ихсановна Хадиева
> Разбаловка
> - 15б за контрольную работу
> - 20б за посещаемость
> - 13б за активность
> ---
> Итого 50б максимум за семестр

---

```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Семинары/Дискретка"
WHERE contains(file.tags, "семинары")
SORT file.cday DESC
```
