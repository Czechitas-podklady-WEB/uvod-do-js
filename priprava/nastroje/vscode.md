## Visual Studio Code

_Visual Studio Code_ je textový editor specializovaný na psaní programů a vývoj software. Obsahuje spoustu pomůcek, nástrojů a rozšíření, která zjednodušují programátorům život a umožňují jim spravovat obsáhlé projekty. VS Code je v současné době jedním z nejpoužívanějších programátorských editorů a mnoho profesionálů jej používá při své práci každý den.

Aktuální verzi editoru si nanistalujte podle instrukcí na [oficiálních stránkách](https://code.visualstudio.com). VS Code je dostupný pro všechny operační systémy.

Pokud máte VS Code nainstalován z dřívějška, zkontrolujte, že máte nejnovější verzi. Z hlavního menu vyberete _Help_ → _Check for Updates…_, VS Code na pozadí stáhne aktuální verzi a nabídne její instalaci.

### Nastavení VS Code

Aby se nám s VS Code pracovalo dobře a zároveň nám všem fungovalo stejně, je potřeba provést základní nastavení. Z hlavního menu vyberete _View_ → _Command Palette..._ a do vyhledávacího políčka napište

```
Open Settings
```

a vyberte položku _Preferences: Open User Settings (JSON)_ viz obrázek.

::fig[Nastavení]{src=assets/nastaveni.png size=85}

Otevře se okno editoru. Jeho obsah smažte a místo něj vložte následující text. Nezapomeňte poté soubor uložit pomocí _File_ → _Save_.

```json
{
	"window.zoomLevel": 0,
	"files.autoSave": "off",
	"files.eol": "\n",
	"files.insertFinalNewline": true,
	"editor.minimap.enabled": false,
	"editor.tabSize": 2,
	"editor.links": false,
	"editor.renderWhitespace": "boundary",
	"editor.wordWrap": "on",
	"editor.fontSize": 16,
	"editor.multiCursorModifier": "alt",
	"editor.formatOnSave": true,
	"editor.bracketPairColorization.enabled": true,
	"editor.guides.bracketPairs": "active",
	"editor.defaultFormatter": "esbenp.prettier-vscode",
	"explorer.compactFolders": false,
	"[html]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[javascript]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[javascriptreact]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[css]": {
		"editor.defaultFormatter": "vscode.css-language-features"
	},
	"prettier.singleQuote": true,
	"prettier.arrowParens": "always",
	"prettier.trailingComma": "all"
}
```
