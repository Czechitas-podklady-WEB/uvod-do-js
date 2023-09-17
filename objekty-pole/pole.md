## Pole

Podobně jako objekty, pole nám :term{cs="Pole" en="Array"} nám umožňují dát našim datům nějakou strukturu. Pole si můžete představit jednoduše jako seznam hodnot. Tvoříme je pomocí hranatých závorek. Takto například do jedné proměnné uložíme známky ze všech písemek psaných za jedno pololetí.

```js
const marks = [3, 1, 2, 4];
```

Uvnitř polí je možné mít zcela libovolné hodnoty, tedy například řetězce, pravdivností hodnoty apod.

```js
const temperatures = [13.5, 12.7, 11.2, 12.3, 15.1];
const users = ['john', 'sue', 'peter', 'jane', 'soji'];
```

Pozor na to, že podobně jako existuje prázný řetězec `''`, existuje také prázdné pole `[]`. Je to zcela běžná hodnota, která se často velmi hodí.

### Indexy

Hodnoty uvnitř polí sídlí na takzvaných indexech. Na jednotlivé indexy přistupujeme také pomocí hranatých závorek. Čeká nás však zajímavé překvapení. 

:::warn
Programátoří vždy počítají od nuly. První prvek pole tedy má index 0, druhý prvek má index 1, třetí prvek má index 2 atd.
:::


```js
const marks = [3, 1, 2, 4];
marks[0] // ⟶ 3
marks[3] // ⟶ 4
```

Pomocí indexů také můžeme hodnoty uvnitř pole měnit. Dejme tomu, že si poslední nehezkou čtyřku opravíme na dvojku.

```js
marks[3] = 2;
marks // ⟶ [3, 1, 2, 2]
```

Všimněte si, že pole může obsahovat libovolné hodnoty, tedy napříkla i objekty. Taková věc se nám může velmi hodit například pro reprezentaci naší tabulky útrat:

```js
const vydaje = [
  { jmeno: 'Petr', zbozi: 'Prací prášek', cena: 240 },
  { jmeno: 'Ondra', zbozi: 'Savo', cena: 80 },
  { jmeno: 'Pavla', zbozi: 'Toaleťák', cena: 65 },
  { jmeno: 'Zuzka', zbozi: 'Mýdlo', cena: 50 },
  { jmeno: 'Pavla', zbozi: 'Závěs do koupelny', cena: 350 },
  { jmeno: 'Libor', zbozi: 'Pivka na kolaudačku', cena: 124 },
  { jmeno: 'Petr', zbozi: 'Pytle na odpadky', cena: 75 },
  { jmeno: 'Míša', zbozi: 'Utěrky na nádobí', cena: 130 },
  { jmeno: 'Ondra', zbozi: 'Toaleťák', cena: 120 },
  { jmeno: 'Míša', zbozi: 'Pečící papír', cena: 30 },
  { jmeno: 'Zuzka', zbozi: 'Savo', cena: 80 },
  { jmeno: 'Petr', zbozi: 'Tapeta na záchod', cena: 315 },
  { jmeno: 'Ondra', zbozi: 'Toaleťák', cena: 6 },
];
```

K jednotlivým hodnotám se dostaneme pomocí indexů a klíčů. Takto například vypíšeme, kolik utratil Ondra za savo

```js
vydaje[1].cena // ⟶ 80
```

### Vlastnosti a metody

Pole také mají zajímavé vlastnosti a metody. Vlastnost `length` udává, kolik prvků se v poli nachází.

```js
marks.length // ⟶ 4
```

Pomocí metody `push` můžeme přidat novou hodnotu na konec pole.

```js
marks.push(1);
marks // ⟶ [3, 1, 2, 2, 1]
```

Naopak pomocí metody `pop` poslední prvek pole smažeme. Exitují také metody `shift` a `unshift`, které přidávají a odebírají prvky ze začátku pole.

Pomocí metody `includes` můžeme zjistit, jestli se uvnitř pole nachází zadaný prvek.

```js
marks // ⟶ [ 1, 1, 2, 2 ]
marks.includes(1) // ⟶ true
marks.includes(3) // ⟶ false
```

Metoda `indexOf` nám přímo řekne první index, na kterém se zadaný prvek v poli nachází. Pokud prvek v poli není, obdržíme -1.

```js
marks // ⟶ [ 1, 1, 2, 2 ]
marks.indexOf(2) // ⟶ 2
marks.indexOf(3) // ⟶ -1
```
