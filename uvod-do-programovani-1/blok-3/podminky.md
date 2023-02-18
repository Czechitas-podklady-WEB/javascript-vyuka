## Podmínky

### Základní variant

```js
let vek = 6

if (vek < 18) {
	console.log('Podmínka platí')
}
```

Vykoná kód ve složených závorkách pouze v případě, že podmínka `(vek < 18)` platí.

### Varianta s `else`

```js
let vek = 6

if (vek < 18) {
	console.log('Podmínka platí')
} else {
	console.log('Podmínka neplatí')
}
```

Definuje, co se má stát i v případě, že podmínka neplatí.
