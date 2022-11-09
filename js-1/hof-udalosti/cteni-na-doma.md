## Povinné čtení na doma

### Rušení časovačů

Pokud spustíme nějaký časovač, často jej také chceme po určité době zrušit. Vyrobme například časovač, který každé 3 vteřiny řekne 'ahoj'.

```js
const sayHello = () => {
	document.body.innerHTML += '<p>ahoj</p>'
}

const timerId = setInterval(sayHello, 5000)
```

Všimněte si, že tentokrát jsme si uložili hodnotu, kterou funkce `setInterval` vrací. Tato hodnota je číslo identifikující náš časovač. Pokud kdykoliv chceme, aby časovač přestal běžet, stačí zavolat funkci `clearInterval` s identifikátorem našeho časovače.

```js
clearInterval(timerId)
```

Takto se dá předčasně zrušit i časovač vyrobený pomocí `setTimeout`. Musíme však použít metodu `clearTimeout`.

```js
const showHello = () => {
	document.body.innerHTML += '<p>ahoj</p>'
}

const timerId = setTimeout(showHello, 5000)

const dismissTimer = () => {
	clearTimeout(timerId)
}

setTimeout(dismissTimer, 2000)
```

Tento kód zařídí, že první časovač vůbec neproběhne. Jeho čas je nastaven na 5 vteřin. Už za dvě vteřiny se však spustí druhý časovač, který nekompromisně vypne ten první dřív, než stačil cokoli udělat.
