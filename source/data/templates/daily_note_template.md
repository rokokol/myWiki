|                   Назад | Дальше                  | Оценка |      Тэги      | Трек-настрение |
| -----------------------:|:----------------------- |:------:|:--------------:|:--------------:|
| [[{{date:YYYY-MM-DD}}]] | [[{{date:YYYY-MM-DD}}]] |  #f10  | #y{{date:YYYY}} |      ---       |

# ...

---

# Photo Dump

```litegal

```

---

# Календарь

```dataview
TABLE WITHOUT ID
file.frontmatter.title AS "События"
FROM "Calendar"
WHERE contains(file.name, "{{date:YYYY-MM-DD}}")
SORT file.name ASC
```

---

# Web Dump