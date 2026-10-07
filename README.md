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
| Pagina "contattami" con form e `required` | `contatti.html`, invio tramite Formspree |
| Framework front end | Bootstrap 5.3 (navbar, griglia, form) |
| Favicon | `img/favicon.svg` + `img/favicon.png` |
| Menu sticky | classe `sticky-top` sulla navbar di ogni pagina |
| Flexbox | hero, link social e percorso (`.hero`, `.socials`, `.journey`) |
| CSS Grid | numeri, "cosa porto", skill, progetti, layout del CV (`.stats`, `.values-grid`, `.skills-grid`, `.projects-grid`, `.cv-layout`) |
| Tocco personale | ensō (cerchio zen) animato, etichette fluttuanti, fascia scorrevole: solo CSS, con rispetto di `prefers-reduced-motion` |
| Sass | cartella `scss/` (variabili, mixin, partial, nesting) |
| Open Graph | `<meta property="og:...">` in ogni pagina |
| 100% responsive | mobile first, testato a 390px e 1280px |

## Struttura
```
├── index.html
├── cv.html
├── contatti.html
├── css/style.css        ← generato da Sass, non modificarlo a mano
├── scss/
│   ├── style.scss       ← file principale
│   ├── _variables.scss  ← colori, font, misure
│   ├── _mixins.scss
│   ├── _base.scss
│   ├── _navbar.scss
│   ├── _components.scss
│   └── _home.scss       ← sezioni e animazioni della home
└── img/
```

## Come modificare gli stili
1. Installa in VS Code l'estensione **Live Sass Compiler** (di Glenn Marks)
2. Nelle impostazioni dell'estensione imposta come cartella di output `/css`
3. Apri `scss/style.scss` e clicca **Watch Sass** in basso
4. Ora ogni modifica ai file `.scss` aggiorna automaticamente `css/style.css`

## Pubblicazione con GitHub Pages
1. Crea un nuovo repository pubblico su GitHub
2. Carica tutti i file (con `index.html` nella cartella principale)
3. Vai su **Settings → Pages**
4. In *Source* scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, poi **Save**
5. Dopo un paio di minuti il sito è online all'indirizzo mostrato in quella pagina
