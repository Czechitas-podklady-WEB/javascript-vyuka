## Struktura adresářů

Adresáře, neboli složky můžeme procházet podobně jako to znáte z aplikace _Průzkumník_/_Explorer_ i pomocí příkazové řádky.

### Užitečné termíny

- :term{cs="Stromová struktura" en="tree structure"} popisuje rozložení, zanořování složek do sebe. Složku si můžeme představit jako větev a složky a soubory uvnitř ní jako její menší větvičky.

- :term{cs="Kořen" en="root"} označuje nejhlavnější složku na vašem disku, ve které jsou zanořené všechny ostatní. Kořenová složka se často říká také té, ve které jsou všechny soubory a složky jednoho projektu, jednoho webu typicky se souborem `index.html` na nejvyšší úrovni, v kořeni.

### Příkazová řádka

#### Výpis souborů a složek v aktuální složce

- ##### Mac

  ```sh
  ls
  ```

- ##### Windows

  ```sh
  dir
  ```

#### Přesun do zanořené složky

- ##### Mac i Windows

  ```sh
  cd nazev-slozky
  ```

#### Přesun do rodičovské složky

- ##### Mac i Windows

  (`cd`, mezera a dvě tečky)

  ```sh
  cd ..
  ```

#### Vytvoření další složky

- ##### Mac i Windows

  ```sh
  mkdir nazev-nove-slozky
  ```

#### Otevření textového souboru

- ##### Mac

  ```sh
  open -a TextEdit nazev-souboru.txt
  ```

- ##### Windows

  ```sh
  notepad.exe nazev-souboru.txt
  ```

Pokud soubor `nazev-souboru.txt` neexistuje, příkazem výšeho ho můžete zároveň vytvořit.
