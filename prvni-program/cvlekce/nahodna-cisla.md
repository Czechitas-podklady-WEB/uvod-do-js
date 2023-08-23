---
title: Náhodná čísla
lead: Zobrazte na stránce náhodné číslo
demand: 1
offerSolution: false
---

Založte si JavaScriptový program a pomocí `document.body.innerHTML` a funkce `Math.random` zobrazte na stránce náhodné číslo. Zkuste stránku několikrát po sobě obnovit a ověřte si, že pokaždé obdržíte jiné číslo.

:::solution

```js
document.body.innerHTML = Math.random();
```
:::
