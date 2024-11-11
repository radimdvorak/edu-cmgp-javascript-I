### **JavaScript a HTML DOM: Úvod**

Tento materiál vychází z informací na [JavaScript HTML DOM](https://www.w3schools.com/js/js_htmldom.asp).

### OBSAH
Seznámíte se s:
1. HTML DOM a jeho strukturou
1. přístupem k prvkům DOM
1. změnou prvků
1. vytvářením a mazáním prvků
1. událostmi na stránce a reakcemi na ně
1. příklady
1. s odkazy na další materiály

### **1 Co je HTML DOM?**
Když se načte stránka, prohlížeč vytvoří její model **DOM** (**D**ocument **O**bject **M**odel). 

**Definice**: HTML DOM (**D**ocument **O**bject **M**odel) je standardní objektový model a programové rozhraní pro HTML.
**Funkce**: Umožňuje programům a skriptům dynamicky přistupovat a měnit obsah, strukturu a styl dokumentu.

**Význam HTML DOM pro webové stránky**
- **Interaktivita**: Umožňuje dynamicky měnit obsah a vzhled stránky bez nutnosti jejího znovunačtení.
- **Dynamické aplikace**: Základ pro tvorbu moderních webových aplikací, které reagují na uživatelské akce.

#### **1.1 Struktura HTML DOM**
- **Hierarchie**: Představuje HTML dokument jako stromovou strukturu, kde každý uzel odpovídá části dokumentu (element, atribut, text).
- **Typy uzlů**:
  - **Document**: Kořenový uzel reprezentující celý dokument.
  - **Element**: Každý HTML tag je elementový uzel.
  - **Text**: Obsah uvnitř elementů.
  - **Atribut**: Vlastnosti elementů (např. `class`, `id`).

![Struktura DOM](https://www.w3schools.com/whatis/img_htmltree.gif "Struktura DOM")

*Struktura DOM - převzaté z [w3schools](https://www.w3schools.com/js/js_htmldom.asp)*

#### **1.2 Vztahy mezi uzly**
- **Rodičovský uzel (parent)**: Uzel, který obsahuje jiné uzly.
- **Dětský uzel (child)**: Uzel obsažený v jiném uzlu.
- **Sourozenecké uzly (siblings)**: Uzly na stejné úrovni hierarchie.

### **2 Přístup k HTML prvkům pomocí JavaScriptu**
- **Metody pro výběr prvků**:
  - `document.getElementById('id')`: Výběr prvku podle jeho `id`.
  - `document.getElementsByClassName('class')`: Výběr prvků podle třídy.
  - `document.getElementsByTagName('tag')`: Výběr prvků podle názvu tagu.
  - `document.querySelector('selector')`: Výběr prvního prvku podle CSS selektoru.
  - `document.querySelectorAll('selector')`: Výběr všech prvků podle CSS selektoru.

### **3 Manipulace s HTML prvky**
- **Změna obsahu**:
  - `element.innerHTML = 'Nový obsah';`: Nastaví obsah HTML prvku (můžeme psát kód v HTML).
  - `element.textContent = 'Nový text';`: Nastaví textový obsah prvku (pouze text k zobrazení).
  - [názorná ukázka](https://www.w3schools.com/jsref/prop_node_textcontent.asp) rozdílů.
- **Změna atributů**:
  - `element.setAttribute('atribut', 'hodnota');`: Nastaví hodnotu atributu.
  - `element.getAttribute('atribut');`: Získá hodnotu atributu.
  - `element.removeAttribute('atribut');`: Odstraní atribut.
- **Změna stylů**:
  - `element.style.property = 'hodnota';`: Nastaví konkrétní CSS vlastnost.
- **Příklad:**
  ```javascript
        let reakce = document.getElementById("otazka_reakce");
        reakce.innerHTML = "Správná odpověď.";
        reakce.style.backgroundColor = "white";
        reakce.style.color = "green";
  ```
### **4 Přidávání a odstraňování prvků**
- **Vytvoření nového prvku**:
  - `let novyPrvek = document.createElement('tag');`: Vytvoří nový element.
- **Přidání prvku do dokumentu**:
  - `rodicovskyPrvek.appendChild(novyPrvek);`: Přidá nový prvek jako poslední dítě rodičovského prvku.
- **Odstranění prvku**:
  - `rodicovskyPrvek.removeChild(prvek);`: Odstraní specifikovaný prvek z rodičovského prvku.

### **5 Události a jejich zpracování**
- **Definice události v HTML:**
  - `<button id="zmenText" onclick="zmenaTextu()">Klikni na mě</button>`: Přiřadí funkci `zmenaTextu()` k události kliknutí.
- **Přidání posluchače události (JavaScript)**:
  - `element.addEventListener('typUdálosti', funkce);`: Přidá posluchače pro specifickou událost (např. kliknutí).

### **6 Praktický příklad: Změna textu po kliknutí**
#### 6.1 Propojení událostí s funkcí v HTML
- **HTML**:
  ```html
  <button id="zmenText" onclick="zmenaTextu()">Klikni na mě</button>
  <p id="text">Původní text.</p>
  ```
- **JavaScript**:
  ```javascript
  function zmenaTextu() {
    let odstavec = document.getElementById('text');
    odstavec.textContent = 'Text byl změněn!';
  }
  ```

#### 6.2 Propojení událostí s funkcí v JavaScriptu
- **HTML**:
  ```html
  <button id="zmenText">Klikni na mě</button>
  <p id="text">Původní text.</p>
  ```
- **JavaScript**:
  ```javascript
  let tlacitko = document.getElementById('zmenText');
  let odstavec = document.getElementById('text');

  tlacitko.addEventListener('click', function() {
    odstavec.textContent = 'Text byl změněn!';
  });
  ```

### **7 Další materiály**
- **Interaktivní tutoriály**: [W3Schools](https://www.w3schools.com/js/js_htmldom.asp) poskytuje praktické ukázky a možnost vyzkoušet si kód online.
- **Oficiální dokumentace**: [MDN Web Docs](https://developer.mozilla.org/cs/docs/Web/API/Document_Object_Model) nabízí podrobné informace a příklady.
