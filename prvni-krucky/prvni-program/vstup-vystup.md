V minulé lekci jsme si malinko osahali příkazy v JavaScriptu, ale zatím jsme ještě nenapsali žádny opravodý program. Jelikož je JavaScript jazyk webu, je potřeba si nejdříve založit webovou stránku.

## Webové stránky

Při tvorbě každé webové stránky se spolu s JavaScriptem používají ještě dva další speciální jazyky jménem HTML, CSS. S trochou cviku se můžete naučit základy obou těchto jazyků a začít tvorit vlastní webové stránky.

::fig[webové jazyky]{src=assets/web.png}

HTML (_HyperText Markup Language_) se používá pro tvorbu struktury webové stránky. Pomocí HTML značek se definuje obsah stránky, jako jsou nadpisy, odstavce, obrázky a odkazy. Tyto značky jsou obklopeny hranatými závorkami `< >` a mají až na výjimky) otvírací a zavírací značku. Například takto se v HTML vytvoří nadpis stránky:

```html
<h1>Moje první stránka</h1>
```

CSS (_Cascading Style Sheets_) se používá pro popis toho, jak má stránka vypadat, tedy například barvy, velikosti a typografie. Takto například řekneme, že naše stránka má používat bezpatkové písmo.

```css
html {
  font-family: sans-serif;
}
```

JavaScript pak dodá naším stránkám interaktivitu. Pomocí JavaScriptu můžeme přidat například animace, validace formulářů a změna obsahu stránky po kliknutí na tlačítko. JavaScript může být také použit pro komunikaci s webovými službami a vytváření dynamických webových aplikací.

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

Nyní můžete soubor `index.html` otevřít v prohlížeči Chrome a pokochat se svojí první webovou stránkou.

Tajemný JavaSciptový příkaz

```js
document.body.innerHTML += '<p>JavaScript je super!</p>';
```

si vysvětlíme malinko později.
