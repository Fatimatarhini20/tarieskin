# Tarieskin hjemmeside

Statisk hjemmeside til skønhedsklinikken Tarieskin. Ren HTML og CSS, ingen build og ingen afhængigheder.

## Filer

| Fil | Indhold |
| --- | --- |
| `index.html` | Forside: hero, behandlinger, priser, book tid og kontakt |
| `behandlinger.html` | Underside med en sektion for hver behandling |
| `style.css` | Al styling for begge sider |
| `assets/` | Logo (champagne til lys baggrund, lys udgave til mørk baggrund) |

## Kør lokalt

Åbn `index.html` i en browser. Skrifttyperne (Cormorant Garamond og DM Sans) hentes fra Google Fonts, så der skal være internet for at se dem.

## Responsivt layout

Layoutet er mobile-venligt og bygger på flexbox og CSS grid, så sektionerne ombrydes af sig selv. Det meste ligger i `style.css`:

- `:root` øverst: farver, skrifttyper, sidebredde og sidemargen (`--gutter`)
- `@media (max-width: 600px)` nederst: justeringer til mobil
- Overskrifter bruger `clamp()`, så de skalerer mellem mobil og pc

Tilføj flere breakpoints i bunden af `style.css`, fx til tablet:

```css
@media (max-width: 900px) { /* tablet */ }
```

## Det der mangler at blive udfyldt

Søg efter tekst i firkantede parenteser i begge HTML-filer: `[PRIS]`, `[VARIGHED]`, `[ADRESSE]`, `[POSTNR]`, `[BY]`, `[TELEFONNUMMER]`, `[ÅBNINGSTIDER]`.

"Book tid"-knapperne i kontaktsektionen linker til `#kontakt`. Skift `href` til jeres bookingsystem.

## Billeder af behandlingerne

Behandlingerne bruger i dag buede farveflader med ikoner. Læg fotos i `assets/` og sæt dem ind i stedet:

- Forsidens kort: `<div class="card__visual"><img src="assets/ansigtsbehandling.jpg" alt="Ansigtsbehandling"></div>`
- Undersiden: `<div class="frame"><img src="assets/ansigtsbehandling.jpg" alt="Ansigtsbehandling"></div>`

## Udgiv på GitHub Pages

1. Læg filerne i roden af repositoriet og push til `main`.
2. Gå til Settings, Pages, og vælg "Deploy from a branch", branch `main` og mappen `/ (root)`.
3. Siden er live på `https://<brugernavn>.github.io/<repo>/` efter et minut eller to.
