---
title: Tabule
demand: 3
---

Ve třídě na vysoké škole je 100 studentů. Každý sedí na židli označené číslem postupně od jedné do sta. Vyučující má na své židli číslo nula. Napiště kód, který **náhodně vylosuje číslo od nuly do sta** a tím rozhodne, kdo na konci lekce umyje tabuli. **Vybrané číslo židle vypište do konzole**.

```text
Tabuli dnes umyje student nebo vyučující na židli číslo X
```

---solution

#### Základní varianta

Jednodušší kód, kde má vyučující a poslední student menší šanci na zvolení.

```js
let cisloZidle = Math.round(Math.random() * 100)

console.log(
	'Tabuli dnes umyje student nebo vyučující na židli číslo ' + cisloZidle
)
```

#### Těžší varianta

Vyrovnaná šance pro všechny.

```js
let cisloZidle = Math.round(Math.random() * 101 - 0.5)

console.log(
	'Tabuli dnes umyje student nebo vyučující na židli číslo ' + cisloZidle
)
```
