# Tarieskin – hjemmeside

Almindelig HTML og CSS. Ingen build, ingen frameworks. Åbn `index.html` i en browser for at se siden.

## Filer

| Fil | Indhold |
| --- | --- |
| `index.html` | Forside: hero, behandlingskort, priser, kontakt |
| `behandlinger.html` | Alle 10 behandlinger i 3 kategorier |
| `om-mig.html` | Om mig og min baggrund, Min vision |
| `style.css` | Al styling, delt af alle sider |
| `logo-champagne.png`, `logo-light.png` | Logoer |
| `CNAME` | Domænet `www.tarieskin.dk` (GitHub Pages) – må ikke slettes |
| `Main.dc.html`, `react*.js`, `support.js`, to `.png` med lange navne | Gammelt designudkast. Bruges ikke af siden og kan slettes |

## Til udviklere: layout på mobil, tablet og pc

- Farver, skrifttyper og sidebredde ligger som variabler øverst i `style.css` (`:root`).
- Layoutet bruger flex og grid med `flex-wrap`, så kolonner brydes af sig selv på smalle skærme.
- Der er ét breakpoint til mobil: `@media (max-width: 600px)` nederst i `style.css`. Tilføj flere der, hvis tablet skal justeres.
- Skrifter: Cormorant Garamond og DM Sans fra Google Fonts.

## Indhold der skal opdateres

- Booking: alle "Book tid"-knapper peger på https://tarieskin.planway.com/ og åbner i ny fane.
- Priser: står både i `index.html` (prislisten) og `behandlinger.html`. Ret begge steder.
- Åbningstider og kontaktoplysninger: nederst på hver side (sektionen `#kontakt`).
- Billeder: der er endnu ingen fotos. Se kommentarerne i HTML-filerne for hvor et foto kan sættes ind i stedet for ikon/logo (`assets/foto.jpg`).
- Facebook-linket (`facebook.com/tarieskin`) er et gæt og skal tjekkes.

## Udgivelse

Siden udgives med GitHub Pages: Settings → Pages → Deploy from a branch → `main` / `(root)`.
