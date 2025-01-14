---
tags:
  - dataview-query
---
```dataviewjs
let areaPages = dv.pages('"2. Structured Data"').where(p => JSON.stringify(p.type).includes("5. Types/Quest"))

let areaPage = areaPages[0];

let pages = dv.pages();
let target = dv.pages("#eldorado");

if (areaPage.resident != "") {
	target = dv.pages().where(r => r.link == areaPage.resident)
}

dv.list([areaPage.resident])
dv.list([target])

//dv.list(areaPageLink)
//dv.list(areaPages)

//dv.list(dv.pages('"2. Structured Data"').file.name)
```
