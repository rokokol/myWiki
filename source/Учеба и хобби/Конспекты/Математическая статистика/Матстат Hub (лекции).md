---
tags:
  - "#y2025"
  - матстат
  - учеба
created: 2025-03-17
aliases: 
icon: LiChartCandlestick
---
# Лекции по математической статистике:
> Технически, я должен изучать это в ВУЗе. Но наши лекции полная хуйня. Если каким-то невероятно-неведанным образом они понадобятся хоть кому-нибудь, то [[Лекции Дубровина|вот (тык)]]

## МФТИ
> Крутые лекции есть и у физтеха
```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Конспекты/Математическая статистика"
WHERE contains(file.tags, "мфти") AND
contains(file.tags, "конспекты")
SORT file.cday DESC
```

## MIT
> Я начал конспектировать только с 6 лекции. Тем не менее, самое интересное все равно начинается лишь с 5; Пока что понял что слишком муторно и решил сначала у МФТИ посмотреть курс
```dataview
TABLE WITHOUT ID
  file.link AS "Занятие",
  file.size AS "Объем",
  file.frontmatter.created AS "Дата"
FROM "Учеба и хобби/Конспекты/Математическая статистика"
WHERE contains(file.tags, "mit") AND
contains(file.tags, "конспекты")
SORT file.cday DESC
```