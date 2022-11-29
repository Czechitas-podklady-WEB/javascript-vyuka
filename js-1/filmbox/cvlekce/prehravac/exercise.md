---
title: 'Bonus: Vlastní ovládání přehrávače'
demand: 4
---

Obohaťte video přehrávač vlastními ovládacími prvky.

1. V souboru `film.html` u prvku `<video>` umažte ručně atribut `controls`. Skyjí se tím ovládací prvky předchystané přímo prohlížeče. V CSS je pak předchystaný kód, který automaticky zobrazí `<div class="player-controls">` s vlastním vizuálem. Vy v CSS nemusíte nic měnit. Jen si všimněte, že se na stránce objevily jiné ovládací prvky, které ale nereagují na klikání.

1. Oživte tlačítko pro přehrávání a pozastavení.

   1. Ve `script.js`, pokud je na stránce prvek s id `prehravac`, přidejte posluchač události kliknutí na prvek se třídou `play`.

   1. Na kliknutí zavolejte na prvku `<video>` metodu `.play()`. Pokud uživatel klikne, video by se mělo začít přehrávat.

   1. Přidejte na `<video>` posluchač události `playing`. Ta nastává v okamžiku, kdy se video začíná přehrávat.

   1. Při události na prvku s id `prehravac` přidejte třídu `playing`. Předchystané CSS v takovém případě zařídí, že se přehrávací tlačítko skryje a místo něho se objeví tlačítko pro pozastavení.

   1. Tlačítku `.pause` přidejte posluchač, který po kliknutí zavolá na videu metodu `.pause()`, což pozastaví přehrávání.

   1. Poslouchejte na událost s názvem `pause`. Pokud nastane, odeberte z přehrávače třídu `playing`.

1. V prvku se třídou `current-time` zobrazujte aktuální čas přehrávaného videa.

   1. Poslouchejte na prvku videa událost `timeupdate`. Pokud nastane, vyčtěte z videa přes vlastnost `.currentTime` počet přehraných sekund.

   1. Aktuální čas zaokrouhlete a převeďte zvlášť na minuty a sekundy.

   1. Obě hodnoty oddělené dvojtečkou vypište do prvku `.current-time`.

#### Bonus

1. Spusťte/pozastavte přehrávání, pokud uživatel na stránce zmáčkne klávesu mezerní.

1. Všimněte si, že video se pozastavuje a přehrává, když uživatel píše do formuláře pro poznámku text a dělá u toho mezery. Spusťte/pozastavte přehrávání pouze v případě, že uživatel nebyl ve formuláři, když mačkal mezerník.

   ```js
   if (
   	event.code === 'Space' &&
   	event.target.tagName !== 'TEXTAREA' &&
   	event.target.tagName !== 'INPUT' &&
   	event.target.tagName !== 'BUTTON'
   ) {
   	// …
   }
   ```

#### Extra bonus

Skryjte ovládací panel, pokud uživatel po dobu tří sekund nepohnul myší ani nestiskl žádnou klávesu.

Ovládací panel skryjete přidáním třídy `hidden` na prvek se třídou `player-controls`.

::fig[řešení]{src=assets/reseni.gif}

---solution

Všechny úlohy mají jedno společné vypracované řešení zde [github.com/Czechitas-podklady-WEB/FilmBox/tree/reseni](https://github.com/Czechitas-podklady-WEB/FilmBox/tree/reseni).
