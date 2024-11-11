
### **Tahák HTML**

#### Komplexní zdroj informací
Pamatujte, tento tahák je pouze úvodním přehledem. Web w3schools poslouží jako výborný komplexní zdroj informací k HTML, kde lze také přímo interaktivně HTML stránky zkoušet.
https://www.w3schools.com/html/default.asp

#### **1. HTML (HyperText Markup Language)**
- Základní jazyk pro tvorbu webových stránek.
- Používá **značky (tagy)** k popisu struktury a obsahu stránky.

#### **2. Základní struktura HTML dokumentu**

```html
<!DOCTYPE html>  <!-- Deklarace dokumentu, říká prohlížeči, že jde o HTML -->
<html lang="cs"> <!-- Kořenový tag pro HTML dokument, atribut lang určuje jazyk -->
  <head>         <!-- Hlavička dokumentu, obsahuje metadata -->
    <meta charset="UTF-8">  <!-- Nastavení kódování, UTF-8 je doporučené -->
    <title>Stránka</title>  <!-- Název stránky, zobrazuje se na kartě prohlížeče -->
  </head>
  <body>               <!-- Tělo stránky, obsahuje viditelný obsah pro uživatele -->
    <h1>Vítejte!</h1>  <!-- Nadpis první úrovně -->
    <p>Toto je odstavec textu.</p>   <!-- Odstavec textu -->
  </body>
</html>
```

#### **3. Klíčová terminologie**

- **Tagy (značky)**: Značky obklopují obsah a říkají prohlížeči, jak ho zobrazit. Příklad: `<h1>`, `<p>`, `<a>`.
- **Element**: Kombinace otevíracího a uzavíracího tagu a obsahu mezi nimi, např. `<p>Toto je text.</p>`.
- **Atributy**: Dodatečné informace pro tag, obvykle ve formátu `název="hodnota"`. Příklad: `<a href="https://example.com">Odkaz</a>`.
- **Obsah**: Text nebo další HTML prvky mezi otevíracím a zavíracím tagem.

#### **4. Základní tagy**

- **`<h1> až <h6>`**: Nadpisy různé úrovně, kde `<h1>` je největší a `<h6>` nejmenší.
- **`<p>`**: Odstavec textu.
- **`<a href="URL">`**: Odkaz na jinou stránku nebo část webu.
- **`<img src="adresa_obrázku" alt="popis_obrázku">`**: Vložení obrázku, atribut `alt` je popis obrázku (důležitý pro přístupnost).
- **`<ul>`, `<ol>`, `<li>`**: Nečíslovaný seznam (unordered list), číslovaný seznam (ordered list), položka seznamu.
  
  ```html
  <ul>
    <li>Položka 1</li>
    <li>Položka 2</li>
  </ul>
  ```

- **`<div>`**: Obalový element pro seskupení obsahu, obvykle pro styly a rozložení.
- **`<span>`**: Podobné jako `<div>`, ale používá se pro kratší části textu.

#### **5. Příklady dalších běžných tagů**

- **Formuláře**: Základní formulářový prvek, obsahuje vstupní pole, tlačítka apod.

  ```html
  <form action="/odeslat" method="post">
    <label for="jmeno">Jméno:</label>
    <input type="text" id="jmeno" name="jmeno">
    <button type="submit">Odeslat</button>
  </form>
  ```

- **Komentáře**: Poznámky v kódu, které nejsou viditelné pro uživatele.

  ```html
  <!-- Toto je komentář -->
  ```

#### **6. Strukturování stránky s div a span**

- **`<div>`** se používá pro rozdělení velkých bloků obsahu.
- **`<span>`** je pro kratší části textu, např. pro zvýraznění určitého slova.

  ```html
  <div>
    <h2>Nadpis</h2>
    <p>Odstavec s <span>zvýrazněným textem</span>.</p>
  </div>
  ```

#### **7. Užitečné atributy**

- **`id`**: Unikátní identifikátor elementu, užitečné pro CSS a JavaScript.
- **`class`**: Identifikuje skupinu elementů se stejným stylem nebo chováním.

#### **8. Tipy**

- **Ukládejte změny a aktualizujte stránku**: Po úpravě HTML dokumentu uložte změny a aktualizujte stránku (F5 nebo Ctrl + R).
- **Zkoušejte kód v prohlížeči**: Používejte vývojářské nástroje (F12) pro kontrolu a experimentování s kódem v prohlížeči.

---

### **Tahák (HTML5)**

#### **1. HTML5 a nové strukturální tagy**
- HTML5 přináší nové tagy, které zlepšují strukturu webových stránek a usnadňují čtení kódu jak pro vývojáře, tak pro prohlížeče.
- Hlavní strukturální tagy HTML5:

  - **`<header>`**: Záhlaví stránky nebo sekce (např. s logem nebo navigací).
  - **`<nav>`**: Sekce pro navigační odkazy.
  - **`<section>`**: Logická část stránky, obvykle s vlastním obsahem na konkrétní téma.
  - **`<article>`**: Samostatný obsah, např. příspěvek na blogu.
  - **`<aside>`**: Vedlejší obsah, například postranní panel.
  - **`<footer>`**: Zápatí stránky nebo sekce, obvykle s kontakty nebo odkazy.

  ```html
  <header>
    <h1>Moje webová stránka</h1>
    <nav>
      <a href="#domu">Domů</a>
      <a href="#o_nas">O nás</a>
    </nav>
  </header>
  
  <section>
    <h2>Hlavní obsah</h2>
    <p>Toto je hlavní část stránky.</p>
  </section>
  
  <aside>
    <h3>Vedlejší informace</h3>
    <p>Dodatečný obsah nebo odkazy.</p>
  </aside>
  
  <footer>
    <p>&copy; 2023 Moje webová stránka</p>
  </footer>
  ```

#### **2. Multimedia v HTML5**

- **`<audio>`**: Vloží zvukový soubor s možností ovládání.

  ```html
  <audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Váš prohlížeč nepodporuje přehrávání zvuku.
  </audio>
  ```

- **`<video>`**: Vloží video s možností přehrávání.

  ```html
  <video controls width="320" height="240">
    <source src="video.mp4" type="video/mp4">
    Váš prohlížeč nepodporuje přehrávání videa.
  </video>
  ```

#### **3. Formulářové prvky HTML5**

HTML5 přidává nové typy vstupních polí, která zjednodušují validaci a zadávání údajů:

- **`<input type="email">`**: Kontroluje zadání e-mailové adresy.
- **`<input type="tel">`**: Specifikuje vstup pro telefonní číslo.
- **`<input type="date">`**: Výběr data pomocí kalendáře.
- **`<input type="range">`**: Posuvník s hodnotami.

  ```html
  <form>
    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email">
    
    <label for="datum">Datum narození:</label>
    <input type="date" id="datum" name="datum">
    
    <label for="hlaseni">Hlasitost:</label>
    <input type="range" id="hlaseni" name="hlaseni" min="0" max="10">
  </form>
  ```

#### **4. Tagy pro lepší sémantiku**

- **`<main>`**: Hlavní obsah stránky, který by měl být jedinečný pro každou stránku (používá se jen jednou).
- **`<mark>`**: Zvýrazňuje text, který je důležitý, nebo obsah, který uživatelé hledají.
- **`<time>`**: Časová značka, lze použít s atributem `datetime` pro specifikaci přesného času nebo data.

  ```html
  <main>
    <h1>Článek</h1>
    <p>Text s <mark>důležitými</mark> informacemi.</p>
    <time datetime="2023-05-15">15. května 2023</time>
  </main>
  ```

#### **5. Canvas a SVG pro grafiku**

- **`<canvas>`**: Používá se k vykreslování grafiky pomocí JavaScriptu, např. pro animace nebo hry.
  
  ```html
  <canvas id="myCanvas" width="200" height="200"></canvas>
  ```

- **`<svg>`**: Vektorová grafika přímo v HTML, skvělá pro tvary a ikony.

  ```html
  <svg width="100" height="100">
    <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
  </svg>
  ```

#### **6. Další vylepšení v HTML5**

- **`data-*` atributy**: Umožňují ukládat vlastní data do HTML elementů, což je užitečné pro interakce pomocí JavaScriptu.

  ```html
  <div data-user-id="123">Uživatel</div>
  ```

- **Responsivita**: Použití atributů jako `viewport` v `<meta>` tagu pro správné zobrazení na mobilních zařízeních.

  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```
