
### **Tahák JavaScript**

#### Komplexní zdroj informací
Pamatujte, tento tahák je pouze úvodním přehledem. Web w3schools poslouží jako výborný komplexní zdroj informací k JavaScriptu, kde lze také přímo interaktivně kódy v JavaScript zkoušet.
https://www.w3schools.com/js/default.asp

#### **1. Co je JavaScript?**
- JavaScript je programovací jazyk, který přidává interaktivitu na webové stránky.
- Spouští se na straně klienta (v prohlížeči) a umožňuje dynamickou manipulaci s obsahem stránky.

#### **2. Vložení JavaScriptu**

- **Interní JavaScript**: Kód je vložen přímo do HTML dokumentu mezi `<script>` tagy.

  ```html
  <script>
    alert("Ahoj, světe!");
  </script>
  ```

- **Externí JavaScript**: Kód je uložen v externím souboru s příponou `.js`.

  ```html
  <script src="script.js"></script>
  ```

#### **3. Proměnné**

- Proměnné slouží k uložení hodnot. Vytváří se pomocí `let`, `const` nebo `var` (doporučuje se používat `let` a `const`).

  ```javascript
  let jmeno = "Jan";       // Měnitelná proměnná
  const vek = 20;          // Neměnná proměnná
  var mesto = "Praha";     // Starší způsob
  ```

#### **4. Datové typy**

- **String** (řetězec): Text v uvozovkách. `let text = "Ahoj";`
- **Number** (číslo): Celá nebo desetinná čísla. `let cislo = 42;`
- **Boolean** (logická hodnota): `true` nebo `false`.
- **Array** (pole): Seznam hodnot. `let seznam = [1, 2, 3];`
- **Object** (objekt): Složená struktura s vlastnostmi a hodnotami. 

  ```javascript
  let osoba = { jmeno: "Jan", vek: 20 };
  ```

#### **5. Operátory**

- **Aritmetické**: `+`, `-`, `*`, `/`, `%`
- **Porovnávací**: `==`, `!=`, `===`, `!==`, `<`, `>`, `<=`, `>=`
- **Logické**: `&&` (a), `||` (nebo), `!` (ne)

#### **6. Podmínky**

- Používají se k rozhodování na základě podmínek.

  ```javascript
  let vek = 18;
  if (vek >= 18) {
    alert("Jsi dospělý.");
  } else {
    alert("Jsi nezletilý.");
  }
  ```

#### **7. Smyčky**

- **for**: Opakuje kód po určitý počet opakování.

  ```javascript
  let text = "";
  for (let i = 0; i < 5; i++) {
    text += i + " ";
  }
  ```
  Hodnota proměnné `text` po provedení cyklu `for`: `0 1 2 3 4 `

- **while**: Opakuje kód, dokud je podmínka pravdivá.

  ```javascript
  let text = "";
  let i = 4;
  while (i >= 0) {
    text += i + " ";
    i--;
  }
  ```
  Hodnota proměnné `text` po provedení cyklu `while`: `4 3 2 1 0 `

#### **8. Funkce**

- Funkce je blok kódu, který lze opakovaně použít. 

  ```javascript
  function pozdrav(jmeno) {
    return "Ahoj, " + jmeno + "!";
  }
  
  alert(pozdrav("Marie"));
  ```

- **Anonymní a šipková funkce (Arrow Function)**

  ```javascript
  const pozdrav = (jmeno) => "Ahoj, " + jmeno + "!";
  ```

#### **9. Práce s DOM (Document Object Model)**

- DOM umožňuje přistupovat a měnit obsah HTML stránky pomocí JavaScriptu.

  ```javascript
  // Výběr elementu podle ID
  let nadpis = document.getElementById("nadpis");
  nadpis.textContent = "Nový text";

  // Výběr elementů podle třídy
  let paragrafy = document.getElementsByClassName("text");
  paragrafy[0].style.color = "blue";
  ```

#### **10. Události**

- Události reagují na akce uživatele, jako je kliknutí nebo pohyb myší.

  ```javascript
  document.getElementById("tlacitko").addEventListener("click", function() {
    alert("Tlačítko bylo stisknuto!");
  });
  ```

#### **11. Console**

- `console.log()` se používá pro zobrazení zpráv v konzoli, což je užitečné pro ladění kódu.

  ```javascript
  console.log("Zpráva pro ladění");
  ```

#### **12. Časté vestavěné metody**

- **String** metody: `toUpperCase()`, `toLowerCase()`, `includes()`, `slice()`, `split()`
  
  ```javascript
  let text = "Ahoj světe!";
  console.log(text.toUpperCase());
  ```

- **Array** metody: `push()`, `pop()`, `shift()`, `unshift()`, `map()`, `filter()`

  ```javascript
  let cisla = [1, 2, 3];
  cisla.push(4);  // Přidá 4 na konec
  console.log(cisla);
  ```

#### **13. JSON (JavaScript Object Notation)**

- JSON je formát pro výměnu dat, běžně používaný při práci s API.

  ```javascript
  let osoba = { jmeno: "Jan", vek: 20 };
  let osobaJSON = JSON.stringify(osoba);  // Převod na JSON
  let zpetnaOsoba = JSON.parse(osobaJSON);  // Zpětný převod na objekt
  ```

#### **14. Příklad JavaScript kódu**

```javascript
// Změna textu při kliknutí na tlačítko
document.getElementById("zmenText").addEventListener("click", () => {
  let nadpis = document.getElementById("nadpis");
  nadpis.textContent = "Text byl změněn!";
});
```
