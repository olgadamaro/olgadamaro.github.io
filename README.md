# Olga D'Amaro – Sito personale

Progetto HTML e CSS per Start2Impact.

Portfolio personale in HTML, Sass e Bootstrap 5.

🔗 **Sito online:** https://olgadamaro.github.io/

## Pagine
- `index.html` – Home: presentazione, chi sono, skill, progetti
- `cv.html` – Curriculum in HTML
- `contatti.html` – Form di contatto

## Requisiti del progetto e dove trovarli
| Requisito | Dove |
|---|---|
| Almeno 2 pagine + CV in HTML | `index.html`, `cv.html`, `contatti.html` |
| Pagina "contattami" con form e `required` | `contatti.html`, invio tramite Formspree (nessun JavaScript) |
| Framework front end | Bootstrap 5.3.3 **compilato dai sorgenti Sass** con i colori del sito (`scss/_bootstrap.scss`) |
| Favicon | `img/favicon.svg` + `img/favicon.png` |
| Menu sticky | `.site-nav` con `position: sticky` su tutte le pagine |
| Menu mobile senza JavaScript | checkbox + `<label>` e selettori `:checked ~` in `scss/_navbar.scss` |
| Flexbox | hero, percorso, menu (`.hero`, `.journey`, `.site-nav__inner`) |
| CSS Grid | numeri, "cosa porto", skill, caso di studio, layout del CV (`.stats`, `.values-grid`, `.skills-grid`, `.case-study`, `.cv-layout`) |
| Sass | moduli `@use`, variabili, mixin, nesting, BEM, funzioni `color.adjust()` / `color.scale()` |
| Open Graph | `<meta property="og:...">` in ogni pagina |
| 100% responsive | mobile first, testato da 390px a 1440px |
| Accessibilità | contrasti verificati (testo ≥ 4.5:1), focus visibile da tastiera, menu usabile con Tab e barra spaziatrice, `alt`, `prefers-reduced-motion` |

**JavaScript: zero.** Nessuno script viene caricato.

## Struttura
```
├── index.html
├── cv.html
├── contatti.html
├── css/style.css          ← generato da Sass (Bootstrap + stili del sito), non modificarlo a mano
├── scss/
│   ├── style.scss         ← file principale: carica i moduli con @use
│   ├── _variables.scss    ← colori, font, misure, breakpoint
│   ├── _mixins.scss       ← from-md, from-lg, card, flex-center, visually-hidden
│   ├── _bootstrap.scss    ← Bootstrap configurato con i colori del sito
│   ├── _base.scss         ← tipografia, sezioni, focus
│   ├── _navbar.scss       ← menu sticky e apertura su mobile solo CSS
│   ├── _components.scss   ← bottoni, social, skill, caso di studio, form, footer
│   ├── _home.scss         ← hero e sezioni della home, animazioni
│   └── _cv.scss           ← layout del CV e timeline
├── img/
├── package.json           ← Bootstrap 5.3.3 e Sass come dipendenze npm
└── .gitignore             ← esclude node_modules/
```

## Come compilare gli stili
Bootstrap non è copiato nel repository: si installa con npm, come in un progetto professionale.
Serve [Node.js](https://nodejs.org/). Dalla cartella del progetto:

```
npm install      # scarica Bootstrap 5.3.3 e Sass in node_modules/
npm run build    # compila scss/style.scss in css/style.css
npm run watch    # ricompila a ogni modifica
```

Lo script usa `--load-path=node_modules` (per scrivere `@use "bootstrap/scss/bootstrap"`) e `--quiet-deps`, che nasconde gli avvisi interni a Bootstrap 5.3: il codice del sito compila senza alcun warning.

## Pubblicazione con GitHub Pages
1. Crea un nuovo repository pubblico su GitHub
2. Carica tutti i file (con `index.html` nella cartella principale)
3. Vai su **Settings → Pages**
4. In *Source* scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, poi **Save**
5. Dopo un paio di minuti il sito è online all'indirizzo mostrato in quella pagina
