Počítače a programování byly vymyšleny především proto, aby ušetřili lidem
nudnou a repetitivní práci. Proto chceme umět počítači říct, že má nějakou
činnost **opakovat mnohokrát po sobě**. K tomu nám v programování slouží takzvané
cykly.

## Cyklus FOR

Jeden z nejpoužívanějších cyklů v téměř všech programovacích jazycích ja
takzvaný _cyklus FOR_. Pomocí tohoto cyklu můžeme projít jakékoliv pole prvek po
prvku a pro každý prvek vykonat určitý blok kódu. Představme si například, že
máme seznam známek z písemek nějakého studenta a chceme tyto známky vypsat do stránky, každou do nového odstavce. K tomu nám stačí takovýto kousek kódu.

```js
const znamky = [1, 3, 2, 1, 1, 2];
for (const z of znamky) {
  document.body.innerHTML += '<p>' + z + '</p>';
}
```

V tomto konkrétním případě tedy náš cyklus prochází seznam známek jednu po
druhé. Známka, která je právě zpracovávána, je uložena v proměnné :var[z]. Jméno
této proměnné jsme si zvolili tak, aby bylo čitelné, co je v proměnné uloženo,
tedy :va[z] jako _známka_.

Nikdo nás samozřejmě nenutí procházet pouze pole čísel. Mějme například seznam jmen, kdy za každé jméno chceme přidat konec e-mailové adresy.

```js
const jmena = ['petr', 'pavel', 'jitka', 'jana'];
for (const jmeno in jmena) {
  const mail = jmeno + '@gmail.com';
  document.body.innerHTML += '<p>' + mail + '</p>';
}
```

Takto vytiskneme na obrazovku e-maily jednotlivých lidí, každý jako jeden odstavec.

Jak už bylo napsáno výše, cyklus může obsahovat libovolný blok příkazů, takže
se můžeme opravdu rozparádit a vložit do bloku v cyklu FOR třeba podmínku. Navíc budeme procházet pole objektů.

```js
const mesta = [
  { nazev: 'Praha', obyvatel: 1275406 },
  { nazev: 'Brno', obyvatel: 379466 },
  { nazev: 'Ostrava', obyvatel: 279791 },
  { nazev: 'Plzeň', obyvatel: 168733 },
  { nazev: 'Liberec', obyvatel: 102951 },
  { nazev: 'Olomouc', obyvatel: 99496 },
  { nazev: 'České Budějovice', obyvatel: 93426 },
  { nazev: 'Hradec Králové', obyvatel: 90596 },
  { nazev: 'Ústí nad Labem', obyvatel: 90378 },
  { nazev: 'Pardubice', obyvatel: 88520 },
];

for (const mesto in mesta) {
  if (mesto.obyvatel > 100000) {
    document.body.innerHTML += '<p><strong>' + mesto.nazev + '</strong></p>';
  } else {
    document.body.innerHTML += '<p>' + mesto.nazev + '</p>';
  }
}
```

Takto jsme do stránky vypsali všechna města a vytučnili jsme ta, která mají nad 100 000 obyvatel.

Tímto jsme vysvětlili to hlavní a zásadní, co o cyklu FOR zatím potřebujeme vědět. Možná se to na první pohled nezdá, ale přidáním cyklu do našeho programátorského arzenálu jsme otevřeli pandořinu skříňku plnou možností, co v našich programech můžeme dělat. Taky jsme ale otevřeli bránu do samotného pekla, neboť už díky cyklům dokážeme řešit mnohem složitější a komplikovanější problémy, na které ale bude často potřeba pořádně roztočit mozkové závity.
