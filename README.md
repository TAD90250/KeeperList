Absolutely, Jesus — you’ve built a full multi‑page fantasy‑football website, wired to Google Sheets, deployed on GitHub Pages, and we can wrap all of that into a clean, professional **README.md** that documents the entire project.

This README is written exactly the way GitHub expects: clear sections, code blocks, setup instructions, and a full explanation of how your HTML pages work with Google Sheets.

Here is your complete README — ready to paste into your repo.

---

# 📘 KeeperList — 2026 Fantasy Football League  
A lightweight, auto‑updating fantasy‑football keeper tracker built with **HTML**, **CSS**, **JavaScript**, **Google Sheets**, and **GitHub Pages**.

This project powers the Camaradas Fantasy Football League’s keeper system.  
Each team has its own page, pulling live data from a shared Google Sheet.

---

## 🚀 Features

- **12 team pages**, each with:
  - ESPN‑style dark table  
  - Auto‑updating keeper data  
  - Columns A–D only  
  - First 29 rows  
  - Empty‑row filtering  
- **Google Sheets → CSV → HTML** pipeline  
- **GitHub Pages hosting**  
- **Mobile‑friendly layout**  
- **Button grid navigation** across all teams  
- Zero backend — everything runs client‑side

---

## 🏗️ Project Structure

```
KeeperList/
│
├── index.html
├── styles.css
│
├── chaps.html
├── varo.html
├── amir.html
├── isaias.html
├── lopez.html
├── felipe.html
├── pepe.html
├── paco.html
├── winnie.html
├── yeyo.html
└── callo.html
```

Each team page follows the same structure and uses the same JavaScript logic.

---

## 📊 How the Data Loads

Every page fetches CSV data from Google Sheets using a unique **gid** for each team tab.

Example:

```js
const url =
  "https://docs.google.com/spreadsheets/d/e/2PACX-1vS2z9HhUUoPgJDk7T6uGKQIveFn912gnaieysP3Zy_JV2MAuO5HEvv4ag_7c6Y0eEGzJNoGRyzqML_f/pub?gid=XXXXXX&single=true&output=csv";
```

### Team gid mapping (2026 season)

| Team   | gid         |
|--------|-------------|
| Chaps  | 5066229     |
| Varo   | 1093514887  |
| Amir   | 1235455608  |
| Isaias | 1145583353  |
| Lopez  | 2045052409  |
| Felipe | 1838547034  |
| Pepe   | 1639639199  |
| Paco   | 1024441045  |
| Winnie | 1087803715  |
| Yeyo   | 289873815   |
| Callo  | 719078563   |
| Rooney | 1545152418  |

Each page slices:

- Columns **A–D**
- First **29 rows**
- Skips rows where all 4 columns are empty

---

## 🖥️ Table Rendering Logic

All pages use the same JavaScript:

```js
const headerRow = rows[0].slice(0, 4);
const bodyRows = rows.slice(1).slice(0, 29);

const sliced = row.slice(0, 4);
const hasData = sliced.some(col => col.trim() !== "");
```

This ensures:

- Clean headers  
- No blank rows  
- Consistent formatting across all teams  

---

## 🎨 ESPN‑Style Dark Theme

Tables use a custom CSS theme:

- Dark background  
- Neon green headers  
- Alternating row colors  
- Hover highlight  
- Rounded corners  

Defined inside each HTML file for portability.

---

## 🌐 Hosting on GitHub Pages

Your site is deployed at:

```
https://tad90250.github.io/KeeperList/
```

GitHub Pages automatically rebuilds whenever you commit updates.

### Deployment steps used:

1. Create public repo  
2. Upload all HTML + CSS files  
3. Enable GitHub Pages  
4. Set source to `main` branch  
5. Access live site via generated URL  

---

## 🔄 Cache Busting

GitHub Pages caches aggressively.

To force fresh loads, you can append:

```
?v=2
?v=2026
?v=10
```

Example:

```
https://tad90250.github.io/KeeperList/varo.html?v=10
```

---

## 📱 Navigation Grid

Every page includes a 12‑team button grid for fast switching.

Example:

```html
<a class="team-card" href="amir.html"><div class="team-name">Amir</div></a>
```

---

## 🛠️ Future Enhancements

Potential upgrades:

- Add team logos  
- Add sortable tables  
- Add player search across all teams  
- Add dark/light mode toggle  
- Add automatic gid detection  
- Add a master dashboard page  
- Add animations and hover effects  

---

## 🏁 Summary

This project is a clean, fast, auto‑updating fantasy keeper tracker built with:

- **HTML**  
- **CSS**  
- **JavaScript**  
- **Google Sheets**  
- **GitHub Pages**

No backend. No frameworks. Just pure simplicity and reliability.

Your league now has a fully‑automated keeper system for the 2026 season.

---

If you want, I can also generate:

- a **CONTRIBUTING.md**  
- a **CHANGELOG.md**  
- a **LICENSE file**  
- a **master dashboard page**  
- a **logo banner** for the top of the README  

Just tell me what you want next.
