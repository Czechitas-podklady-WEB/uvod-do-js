## Problém spolubydlení

Možná se to nezdá, ale po těch několika lekcích, kterými jste prošli, jste již vybavení téměř všemi nezbytnými technickými dovednostmi k tomu, abyste dokázali naprogramovat řešení našeho problému se spolubydlením ze začátku kurzu. Pravda, po takto krátkém kurzu ještě nemáte dost zkušeností na to, abyste si na výsledný program troufli sami. Když jej ale uvidíte už napsaný, začnete poznávat téměř všechny věci, které jsou v programu použity - proměnné, podmínky, objekty, pole, cykly a další.

## Řešení

Připomeňme si tabulku výdajů, kterou jsme viděli na začátku kurzu.

Jméno | Věc                 | Částka
----- | ------------------- | ------
Petr  | Prací prášek        | 240 kč
Ondra | Savo                | 80 kč
Pavla | Toaleťák            | 65 kč
Zuzka | Mýdlo               | 50 kč
Pavla | Závěs do koupelny   | 350 kč
Libor | Pivka na kolaudačku | 124 kč
Petr  | Pytle na odpadky    | 75 kč
Míša  | Utěrky na nádobí    | 130 kč
Ondra | Toaleťák            | 120 kč
Míša  | Pečící papír        | 30 kč
Zuzka | Savo                | 80 kč
Petr  | Tapeta na záchod    | 315 kč
Ondra | Toaleťák            | 64 kč

Popis řešení v lidské řeči by mohl vypadat například takto:

1. Spočítej kolik každý člen utratil celkem,
1. spočítej průměrnou útratu na jednoho člena,
1. spočítej rozdíly jednotlivých členů proti průměru,
1. všechny peníze těch, kteří zaplatili podprůměr, dej do banku,
1. bank rozděl mezi ty, kteří zaplatili nad průměr.

### JavaScriptový program

Tabulku výdajů budeme reprezenvotat pomocí pole objektů tak, jak jsme to jži viděli v lekci o polích a objektech.

```js
const vydaje = [
  { jmeno: 'Petr', zbozi: 'Prací prášek', utrata: 240 },
  { jmeno: 'Ondra', zbozi: 'Savo', utrata: 80 },
  { jmeno: 'Pavla', zbozi: 'Toaleťák', utrata: 65 },
  { jmeno: 'Zuzka', zbozi: 'Mýdlo', utrata: 50 },
  { jmeno: 'Pavla', zbozi: 'Závěs do koupelny', utrata: 350 },
  { jmeno: 'Libor', zbozi: 'Pivka na kolaudačku', utrata: 124 },
  { jmeno: 'Petr', zbozi: 'Pytle na odpadky', utrata: 75 },
  { jmeno: 'Míša', zbozi: 'Utěrky na nádobí', utrata: 130 },
  { jmeno: 'Ondra', zbozi: 'Toaleťák', utrata: 120 },
  { jmeno: 'Míša', zbozi: 'Pečící papír', utrata: 30 },
  { jmeno: 'Zuzka', zbozi: 'Savo', utrata: 80 },
  { jmeno: 'Petr', zbozi: 'Tapeta na záchod', utrata: 315 },
  { jmeno: 'Ondra', zbozi: 'Toaleťák', utrata: 6 },
];
```

Druhý krok je přeložit lidský popis řešení do JavaScriptového kódu. Takový program by
mohl vypadat například takto:

```html
<script type="module">

const vydaje = [
  { jmeno: 'Petr', zbozi: 'Prací prášek', utrata: 240 },
  { jmeno: 'Ondra', zbozi: 'Savo', utrata: 80 },
  { jmeno: 'Pavla', zbozi: 'Toaleťák', utrata: 65 },
  { jmeno: 'Zuzka', zbozi: 'Mýdlo', utrata: 50 },
  { jmeno: 'Pavla', zbozi: 'Závěs do koupelny', utrata: 350 },
  { jmeno: 'Libor', zbozi: 'Pivka na kolaudačku', utrata: 124 },
  { jmeno: 'Petr', zbozi: 'Pytle na odpadky', utrata: 75 },
  { jmeno: 'Míša', zbozi: 'Utěrky na nádobí', utrata: 130 },
  { jmeno: 'Ondra', zbozi: 'Toaleťák', utrata: 120 },
  { jmeno: 'Míša', zbozi: 'Pečící papír', utrata: 30 },
  { jmeno: 'Zuzka', zbozi: 'Savo', utrata: 80 },
  { jmeno: 'Petr', zbozi: 'Tapeta na záchod', utrata: 315 },
  { jmeno: 'Ondra', zbozi: 'Toaleťák', utrata: 6 },
];

import { mean } from 'https://unpkg.com/simple-statistics@7.8.2/index.js?module';

const seznamJmen = [];
const utraty = [];

for (const vydaj of vydaje) {
  const index = seznamJmen.indexOf(vydaj.jmeno);
  
  if (index > -1) {
    utraty[index] += vydaj.utrata;
  } else {
    seznamJmen.push(vydaj.jmeno);
    utraty.push(vydaj.utrata);
  }
}

const prumernaUtrata = mean(utraty);

for (const jmeno of seznamJmen) {
  const index = seznamJmen.indexOf(jmeno);
  const vyrovnani = Math.round(utraty[index] - prumernaUtrata);

  if (vyrovnani > 0) {
    document.body.innerHTML += '<p>' + jmeno + ' dostane: ' + vyrovnani + '</p>';
  } else {
    document.body.innerHTML += '<p>' + jmeno + ' má dáti: ' + (-vyrovnani) + '</p>';
  }
}

</script>
```

Seznamy v proměnných `seznamJmen` a `utraty` představují tabulku celkových útrat
pro každého jednoho člověka.
