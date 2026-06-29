---
title: שיעורים
layout: default
nav_order: 3
has_children: true
permalink: /lessons/
---

# שיעורים

כאן נמצאים דפי השיעור. כל שיעור הוא קובץ Markdown עצמאי עם front matter בראש הקובץ.

## שיעורים לדוגמה

1. [יסודות Markdown]({{ '/lessons/markdown-basics/' | relative_url }})
2. [תכנון פעילות כיתתית]({{ '/lessons/class-activity/' | relative_url }})

## תבנית קצרה לשיעור חדש

```markdown
---
title: כותרת השיעור
layout: default
parent: שיעורים
nav_order: 3
permalink: /lessons/new-lesson/
---

# כותרת השיעור

כתבו כאן את מטרת השיעור, הפעילות והמשימה.
```
