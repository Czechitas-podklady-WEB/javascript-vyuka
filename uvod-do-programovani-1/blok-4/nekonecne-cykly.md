## Nekonečné cykly

Cyklus může být nekonečný, pokud je podmínka s každou obrátkou splněna. V takovém případě se cyklus opakuje donekonečna.

```js
while (1 < 2) {
	console.log('Ťuk')
}

console.log('Hotovo') // K tomuto řádku se nikdy nedostaneme
```

Nekonečný cyklus se do kódu dostává často omylem, chybou a může nám doslova zavařit. Počítač se při zpracovávání takového cyklu totiž většinou pěkně roztopí 🔥. Proto je dobré si při psaní cyklu vždy zkontrolovat, zda je podmínka nastavena správně a zda se cyklus vůbec může někdy zastavit.

Protože i ten nejlepší programátor úplně běžně dělá chyby, zavedeme si pro účely cvičení pojistku pomocí funkce `confirm`, aby nám naši smyčku nepouštěl Replit automaticky a měli jsme možnost si ji před spuštěním vždy zkontrolovat a případně opravit.

```js
if (confirm('Spustit smyčku?')) {
	while (1 < 2) {
		console.log('Ťuk')
	}
}
```

::fig[volání confirm]{src=assets/confirm.png}
