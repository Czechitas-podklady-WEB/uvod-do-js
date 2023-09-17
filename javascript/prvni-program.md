## První program

Svět programování může ze začátku působit velmi tajemně, plný zlých nástrah a neproniknutelných složitostí. Nutnost zapojovat možná trochu zaprášená zákoutí vašeho mozku může ze začátku být velká výzva. Proto společně vykročíme zvolna a krůček po krůčku. Budeme věnovat náležitou péči každému jednotlivému tématu tak, abyste do něj dokázali skutečně proniknout a nepřipadali si jako na jiné planetě. Vězte, že po chvíli se možná trochu zrezivělá mozkové kolečka začnou točit lehčeji a programování vám bude přinášet velkou radost z tvoření.

Jazyk JavaScript je jedním z nejdůležitějších programovacích jazyků nejen v prostředí webu ale i v IT obecně. Každý programovací jazyk je sada nějakých pravidel, jak sestavovat textové příkazy pro počítač. Pokud chceme, aby náš počítač tyto příkazy vykonal, protřebujeme takzvaný _JavaScript runtime_. To je program, který čte JavaScriptové příkazy a vykonává je. Každý prohližeč obsahuje svůj vlastní JavaScript runtime a proto můžeme naše první JavaScriptové programy spouštět přímo v prohlížeči jako webové stránky.

V minulé lekci jsme si malinko osahali příkazy v JavaScriptu, ale zatím jsme ještě nenapsali žádny opravodý program. Jelikož je JavaScript jazyk webu, je potřeba si nejdříve založit webovou stránku.

### Webové stránky

Při tvorbě každé webové stránky se spolu s JavaScriptem používají ještě dva další speciální jazyky jménem HTML, CSS. S trochou cviku se můžete naučit základy obou těchto jazyků a začít tvořit vlastní webové stránky.

::fig[webové jazyky]{src=assets/web.png}

HTML (_HyperText Markup Language_) se používá pro tvorbu struktury webové stránky. Pomocí HTML značek se definuje obsah stránky, jako jsou nadpisy, odstavce, obrázky a odkazy. Tyto značky jsou obklopeny hranatými závorkami `< >` a mají (až na výjimky) otvírací a zavírací značku. Například takto se v HTML vytvoří nadpis stránky:

```html
<h1>Moje první stránka</h1>
```

CSS (_Cascading Style Sheets_) se používá pro popis toho, jak má stránka vypadat, tedy například barvy, velikosti a typografie jednotlivých prvků vytvořených pomocí HTML. Takto například řekneme, že celá naše stránka má používat bezpatkové písmo.

```css
html {
  font-family: sans-serif;
}
```

JavaScript pak dodá naším stránkám interaktivitu. Pomocí JavaScriptu můžeme přidat například animace, validace formulářů nebo změnu obsahu stránky po kliknutí na tlačítko. JavaScript může být také použit pro komunikaci s webový serverem a vytváření dynamických webových aplikací.

Všechny tyto prvky spojíme do jednoho souboru s názvem `index.html`, který pak můžeme otevřít v prohlížečí.


```html
<html>

<style>
  html {
    font-family: sans-serif;
  }
</style>

<body>
  <h1>Moje první stránka</h1>
</body>

<script>
  document.body.innerHTML += '<p>JavaScript je super!</p>';
</script>

</html>
```

Nyní můžete soubor `index.html` otevřít v prohlížeči a pokochat se svojí první webovou stránkou.

Tajemný JavaSciptový příkaz

```js
document.body.innerHTML += '<p>JavaScript je super!</p>';
```

si vysvětlíme malinko později.

### Středníky

Než rozebereme náš první příklad, všimněte si, že končí středníkem. Takto JavaScript runtime pozná, kde končí jeden příkaz a začíná jiný. Inu, ve skutečnosti by to JavaScript poznal i bez středníků a dokonce bychom je na většině míst ani psát nemuseli. Psaní nebo nepsaní středníků je značně kulturní záležitost, každý na to má svůj názor. Jednou je trendy to, jindy zase ono. My na tomto kurzu budeme středníky používat svědomitě a vám do začátku doporučujeme totéž. Později se jistě sami rozhodnete pro styl, který se vám osobně líbí nejvíce.
