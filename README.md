# 4MEN Lujerului — site

Site de prezentare (o singură pagină, static) pentru frizeria 4MEN din Bulevardul Iuliu Maniu 57, București.

## Ce conține

- Hero cu stare live **Deschis / Închis** (calculată în ora României) și programul zilei
- Meniu de servicii și prețuri
- Recenzii reale (Google / MERO), program pe zile cu ziua curentă evidențiată
- Locație + hartă Google embed și link de navigație
- Blocuri Instagram / Facebook
- Butoane de programare către MERO (`https://mero.ro/p/4men`)
- Date structurate schema.org (`HairSalon`) pentru Google

Fără build, fără dependențe: un singur `index.html` + Google Fonts.

## Cum editezi

Toate datele sunt în `index.html`, marcate clar:

| Ce | Unde |
|---|---|
| Instagram ([@4men.studio](https://www.instagram.com/4men.studio/)) / Facebook ([4menstudio](https://www.facebook.com/4menstudio)) | `const SOCIAL = { ... }` din `<script>` (la final) |
| Telefon (0728 029 916) | caută `tel:+40728029916` (header, card hero, secțiunea Locație, footer, schema.org) |
| Program | obiectul `HOURS` din `<script>` **și** lista `<ul class="hours">` |
| Prețuri / servicii | secțiunea `<!-- SERVICII -->` |
| Adresă / hartă | secțiunea `<!-- LOCATIE -->` (linkul și `iframe`-ul) |
| Link programări | caută `mero.ro/p/4men` |

## Rulare locală

```bash
python3 -m http.server 8000
# http://127.0.0.1:8000
```

## Publicare

GitHub Pages, din branch-ul `main`, rădăcină. Site-ul e live la
`https://nistordaniel06-cpu.github.io/4men-lujerului/`.
