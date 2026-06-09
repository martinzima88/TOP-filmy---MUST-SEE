# Filmový kánon – Interaktivní pracovní list (Návod k použití)

Tento projekt je interaktivní webová aplikace a zároveň tisknutelný pracovní list obsahující profilové medailonky **15 zásadních filmů světové kinematografie**. Každý film je detailně rozebrán (význam, hudba, památná scéna) a obsahuje 3 otázky k zamyšlení pro studenty či filmové nadšence.

---

## 🛠️ Jak stránku spustit a používat lokálně

Spuštění aplikace je extrémně jednoduché a nevyžaduje žádné servery ani instalace:
1. Přejděte do složky s projektem (`Antigravity`).
2. Vyhledejte soubor **`index.html`**.
3. Klikněte na něj pravým tlačítkem a otevřete jej v jakémkoliv moderním webovém prohlížeči (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari).
4. Web se okamžitě načte. Můžete vyhledávat, filtrovat podle žánrů či období, zaškrtávat zhlédnuté filmy nebo psát své odpovědi přímo do textových polí. Vše se automaticky ukládá v prohlížeči.

---

## 💻 Potřebuji GitHub? A jak web zrealizovat (zprovoznit online)?

**Stručná odpověď:** Pro vlastní potřebu (nebo pokud chcete list jen vytisknout) **GitHub nepotřebujete**. Pokud však chcete, aby vaši studenti nebo kolegové přistupovali k rozhraní online na internetu a vyplňovali odpovědi na svých zařízeních, GitHub je ta **nejjednodušší a zcela bezplatná cesta**.

Zde jsou 3 možnosti, jak projekt zrealizovat a distribuovat:

### 1. Možnost: Publikace online přes GitHub Pages (Doporučeno pro online výuku)
GitHub Pages je bezplatná služba pro hostování statických webových stránek.
* **Krok 1:** Založte si bezplatný účet na [github.com](https://github.com).
* **Krok 2:** Vytvořte nový repozitář (klikněte na **New**, pojmenujte ho např. `filmovy-pracovni-list` a nastavte ho jako **Public**).
* **Krok 3:** Nahrajte do repozitáře soubory z vašeho počítače:
  * `index.html`
  * `style.css`
  * `moviesData.js`
  * `cinematic_header.png`
* **Krok 4:** V repozitáři přejděte do **Settings** (Nastavení) -> v levém menu zvolte **Pages**.
* **Krok 5:** V sekci *Build and deployment* pod nadpisem *Branch* vyberte větev `main` (nebo `master`) a klikněte na **Save**.
* **Během 1–2 minut** vám GitHub vygeneruje odkaz (např. `https://vaše-jméno.github.io/filmovy-pracovni-list/`), který můžete poslat komukoliv. Web bude plně funkční a interaktivní.

### 2. Možnost: Distribuce v ZIP archivu (Bez cloudu a registrací)
* Celou složku `Antigravity` zabalte do souboru `.zip` a pošlete ji studentům e-mailem nebo nahrajte do sdíleného disku (Google Drive, MS Teams).
* Studenti si ZIP stáhnou, rozbalí na svém počítači a dvakrát kliknou na `index.html`. Vše jim bude fungovat lokálně v prohlížeči (včetně ukládání odpovědí).

### 3. Možnost: Tištěný papírový pracovní list
Pokud preferujete klasickou papírovou formu:
* Otevřete `index.html` u sebe na počítači.
* Klikněte na zlaté tlačítko **„Tisk / Uložit PDF“** (nebo stiskněte klávesovou zkratku `Ctrl + P`).
* V dialogovém okně tisku zvolte buď vaši fyzickou tiskárnu, nebo možnost **Uložit jako PDF** (Save as PDF).
* **Jak funguje kouzlo tisku?** CSS styl automaticky detekuje tiskový režim:
  * Skryje vyhledávací panel, filtry, tlačítka a zaškrtávací políčka.
  * Přepne černé pozadí na čistě bílé a text na černý (šetrné pro tiskárny).
  * **Textová pole pro odpovědi nahradí linkovanými řádky pro ruční psaní.**
  * Zamezí trhání karet filmů uprostřed stránek, takže každý film má čisté ohraničení.

### 📱 QR kód pro Chromebooky a mobilní zařízení (Interaktivita v hodině)
Aplikace obsahuje inteligentní systém QR kódů, který usnadňuje přechod na jiná zařízení:
* **Při zobrazení na dataprojektoru:** QR kód se zobrazuje přímo v záhlaví stránky. Můžete tak promítnout web na tabuli a žáci si ho jednoduše naskenují svými Chromebooky nebo mobilními telefony, čímž okamžitě otevřou interaktivní list.
* **Při vytištění na papír:** QR kód se vytiskne v záhlaví papírového pracovního listu. Žák pracující na papíře může kód kdykoliv naskenovat, aby si na svém Chromebooku pustil oficiální trailer nebo ukázku k danému filmu.
* **Jak kód funguje:** Pokud běžíte lokálně (`file://`), QR kód zobrazuje pomocný text. Jakmile web nahrajete na internet (např. přes GitHub Pages), systém automaticky rozpozná vaši internetovou adresu a vygeneruje přesný QR kód směřující na vaši online verzi.

---

## 📝 Jak upravit data filmů

Pokud byste chtěli změnit výběr filmů, otázky nebo doprovodné texty, nemusíte zasahovat do složitého HTML kódu. Všechna data jsou přehledně strukturována v souboru:
👉 **`moviesData.js`**

Tento soubor můžete otevřít v jakémkoliv textovém editoru (Poznámkový blok, VS Code) a jednoduše upravit texty v uvozovkách. Například:
```javascript
{
  id: "matrix",
  title: "Matrix",
  // ...
  questions: [
    "Zde je nová otázka pro studenty...",
    // ...
  ]
}
```
Ujistěte se, že zachováte správnou syntaxi JavaScriptu (čárky mezi položkami a uvozovky kolem textů).
