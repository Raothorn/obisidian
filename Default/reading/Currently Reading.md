---
id: Currently Reading
aliases:
  - currently_reading
tags:
  - reading
  - personal
---

```dataview
TABLE WITHOUT ID 
    book_title as Title,
    author as Author,
    date_started as "Date Started",
    "<progress max=" + total_pages + " value=" + current_page + "> </progress> " + round(current_page/total_pages*100) + "%" as Progress
FROM #book 
WHERE 
    date_started <= date(today) and date_finished = null
```
