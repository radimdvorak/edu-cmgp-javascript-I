
### **Tahák CSS**

#### Komplexní zdroj informací
Pamatujte, tento tahák je pouze úvodním přehledem. Web w3schools poslouží jako výborný komplexní zdroj informací k CSS, kde lze také přímo interaktivně styly CSS zkoušet.
https://www.w3schools.com/css/default.asp

#### **1. Co je CSS?**
- **CSS (Cascading Style Sheets)** – jazyk pro popis vzhledu a rozložení HTML dokumentu.
- *Odděluje obsah (HTML) od vzhledu (CSS)*.

#### **2. Základní struktura CSS**

- CSS se obvykle zapisuje ve formátu `selektor { vlastnost: hodnota; }`.
  
  ```css
  h1 {
    color: blue;
    font-size: 24px;
  }
  ```

#### **3. Způsoby vložení CSS**

- **Externí CSS**: Vkládá se z externího souboru s příponou `.css`.

  ```html
  <link rel="stylesheet" href="styl.css">
  ```

- **Interní CSS**: Styl je vložen přímo v HTML dokumentu do `<style>` v sekci `<head>`.

  ```html
  <style>
    p {
      color: green;
    }
  </style>
  ```

- **Inline CSS**: Styl je přímo v elementu HTML.

  ```html
  <p style="color: red;">Text</p>
  ```

#### **4. Selektory**

- **Tag selektor**: Působí na všechny elementy daného typu, např. `p { }` (na všechny odstavce).
- **ID selektor**: Identifikuje konkrétní element podle `id`, používá `#`. 

  ```css
  #hlavni-nadpis {
    color: purple;
  }
  ```

- **Třída (class) selektor**: Používá `.class` pro elementy se stejnou třídou.

  ```css
  .odstavec {
    font-style: italic;
  }
  ```

- **Dědičnost selektorů**: Např. `section p { }` působí na všechny `p` uvnitř `section`.

#### **5. Základní vlastnosti CSS**

- **Barvy**: Nastavují se pomocí názvů, hexadecimálních kódů nebo RGB/rgba.

  ```css
  color: red;
  background-color: #f0f0f0;
  ```

- **Fonty**: Nastavení velikosti, rodiny, stylu.

  ```css
  font-size: 16px;
  font-family: Arial, sans-serif;
  font-weight: bold;
  ```

- **Okraje a odsazení**:

  - **`margin`**: Vnější odsazení (okraj) kolem elementu.
  - **`padding`**: Vnitřní odsazení uvnitř elementu.

  ```css
  margin: 10px;
  padding: 15px;
  ```

#### **6. Box Model**

- Každý element je vnímán jako "box" s následujícími částmi:
  - **Content** (obsah)
  - **Padding** (vnitřní okraj)
  - **Border** (rám)
  - **Margin** (vnější okraj)

  ```css
  .box {
    padding: 10px;
    border: 2px solid black;
    margin: 5px;
  }
  ```

#### **7. Layout vlastnosti**

- **`display`**: Nastavuje zobrazení elementu.

  - `block`: Zobrazí jako blok (zabere celou šířku).
  - `inline`: Zobrazí jako inline prvek (v řádku s ostatními).
  - `flex`: Flexibilní uspořádání, často používané pro rozvržení.

  ```css
  .container {
    display: flex;
  }
  ```

- **`position`**: Umožňuje nastavit umístění elementu.

  - `static`: Výchozí, podle toku dokumentu.
  - `relative`: Relativní k původnímu umístění.
  - `absolute`: Pevně umístěné na stránce, relativní k nejbližšímu nadřazenému prvku.
  - `fixed`: Pevná pozice na obrazovce, i při posouvání stránky.

  ```css
  .fixed-box {
    position: fixed;
    top: 0;
    left: 0;
  }
  ```

#### **8. Barvy a pozadí**

- **`background-color`**: Nastaví barvu pozadí.
- **`background-image`**: Nastaví obrázek jako pozadí.

  ```css
  body {
    background-color: #e0e0e0;
    background-image: url('obrazek.jpg');
  }
  ```

#### **9. Přechody (Transitions)**

- Vytváří hladký přechod mezi dvěma hodnotami.

  ```css
  button {
    transition: background-color 0.3s;
  }
  
  button:hover {
    background-color: lightblue;
  }
  ```

#### **10. Media Queries**

- Používají se k vytváření responzivního designu pro různá zařízení.

  ```css
  @media (max-width: 600px) {
    body {
      font-size: 14px;
    }
  }
  ```

---

### **Příklad CSS kódu**

```css
/* Základní styl pro tělo stránky */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f9;
  color: #333;
}

/* Nadpisy */
h1, h2, h3 {
  color: #5c5c5c;
}

/* Odkazy */
a {
  color: #3498db;
  text-decoration: none;
}

/* Při najetí kurzoru */ 
a:hover {
  color: #1f6391;
}

/* Třídy pro karty */
.card {
  border: 1px solid #ddd;
  padding: 15px;
  margin: 10px;
  background-color: white;
}

.card:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
```
