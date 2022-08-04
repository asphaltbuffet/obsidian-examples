---
date created: Tuesday, August 2nd, 2022 4:54:21 pm
date modified: Tuesday, August 2nd, 2022 4:54:21 pm
tags: index
title: Index of Periodic Notes
---

# Index of Periodic Notes

```dataviewjs

for (let years of dv.pages("#yearly_note").groupBy(p => p.year)) {
    dv.header(3, years.key);
    dv.table(["Year"],
        years.rows
            .sort(k => k.file.link, 'asc')
            .map(k => [k.file.link]))
}

for (let group of dv.pages("#monthly_note").groupBy(p => p.year)) {
    dv.header(3, group.key);
    dv.table(["Month"],
        group.rows
            .sort(k => k.file.link, 'asc')
            .map(k => [k.file.link]))
}
```
