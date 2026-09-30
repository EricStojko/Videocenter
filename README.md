# 🎬 Videocenter - Landing Page

Moderna in odzivna predstavitvena spletna stran (landing page) za **Videocenter Koper** – zanesljiva digitalizacija analognih videokaset (VHS, VHS-C, MiniDV, Hi8, Video8) na USB ključek ali DVD.

Domena produkcije: **[videocenter-koper.web.app](https://videocenter-koper.web.app/)**

---

## 🛠️ Tech Stack & Arhitektura

Projekt je zasnovan kot lahka, hitra in visoko optimizirana statična stran:
- **Frontend:** Vanilla HTML5, CSS3, JavaScript (brez težkih ogrodij ali zapletenih build orodij)
- **Struktura map:**
  - `public/` — Kanonični koren spletne strani (Firebase Hosting root)
    - `index.html` — Slovenska različica
    - `it.html` — Italijanska različica
    - `css/style.css` — Enotna deljena stilska predloga (optimizirano za predpomnjenje v brskalniku)
    - `sitemap.xml` & `robots.txt` — SEO konfiguracija
- **Gostovanje:** Firebase Hosting (brezplačni Spark paket)
- **CI/CD:** GitHub Actions samodejna objava ob potisku na vejo `main`

---

## 🤖 AI-Assisted Development

Ta projekt je bil zgrajen z uporabo modernih pristopov "AI Pair Programminga" (Project IDX, AI Agenti). 

Kot inženir in produktni vodja sem AI orodja uporabil kot pospeševalnik za generiranje osnovne strukture, dizajna in vsebine. Hkrati sem osebno skrbel za arhitekturo, pregled kode (Code Review), odpravljanje hroščev in končno testiranje (QA). Ta repozitorij je praktičen primer moje sposobnosti učinkovitega upravljanja AI orodij za hitro dostavo produkcijsko pripravljenih rešitev.

---

## 🚀 Lokalno Testiranje

Ker gre za statično spletno stran, ne potrebujete posebnih orodij za prevajanje:
1. Klonirajte repozitorij.
2. Odprite mapo v poljubnem urejevalniku kode (VS Code, Cursor, IDX).
3. Zaženite razširitev **"Live Server"** neposredno v mapi `public/` ali na datoteki `public/index.html`.

---

## ⚙️ Samodejna Objava (CI/CD z GitHub Actions)

Za delovanje samodejne objave preko `.github/workflows/firebase-deploy.yml`:
1. V Google Cloud / Firebase konzoli ustvarite servisni račun (Service Account) s pravicami *Firebase Hosting Admin*.
2. Izvozite JSON ključ servisnega računa.
3. V GitHub repozitoriju pojdite pod **Settings -> Secrets and variables -> Actions** in dodajte novo skrivnost:
   - Ime: `FIREBASE_SERVICE_ACCOUNT_VIDEOCENTER_KOPER`
   - Vrednost: Vsebina prenesenega JSON ključa.