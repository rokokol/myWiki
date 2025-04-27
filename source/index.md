---
icon: LiTerminal
aliases:
  - начало
---
# Привет
![[logo.png]]

> [!tip] В общем
> ![[icon.png|128]] Это сайт про [[Я|меня, Илью Лещенко]]. Тут я просто делюсь с миром всяким о себе, веду дневник вот...
> www.ilyushas.online

***Записки за последний месяц сразу ниже*** 🔽
Чувствуй себя как дома. У меня "*дома*" 😉

---

**[[Дашборд.canvas|Дашбордик и делишки тут (тык)]]**

```dataview
TABLE WITHOUT ID file.link AS "Записка",
join(filter(file.tags, (t) => regexmatch("#\\d{1,2}f\\d{1,2}", t)), ", ") AS "Оценка" FROM "" 
WHERE regexmatch("^[0-9]{4}\\-[0-9]{2}\\-[0-9]{2}$", file.name)
AND !contains(file.tags, "hide")
SORT file.name DESC
limit 30
```

---

![[angry_penguin.mp4]]