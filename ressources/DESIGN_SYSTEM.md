# Design System — L'Atelier Connecté

> Document de référence obligatoire pour tout développement sur ce projet.
> Toute modification du site doit respecter ces règles sans exception.

---

## 1. Identité visuelle

**Positionnement :** Artisan numérique local. Chaleureux, simple, humain, sans jargon.
**Tonalité visuelle :** Artisanat moderne. Vert vif (action, fraîcheur) + beige/bois (authenticité, proximité).
**Anti-références :** Pas de look "agence tech" froide. Pas de bleu corporate. Pas de noir pur.

---

## 2. Design Tokens (CSS Variables — NE PAS MODIFIER)

```css
:root {
    --primary-color:  #7ed957;  /* Vert vif — CTA, icônes, accents d'action */
    --primary-dark:   #5fb83a;  /* Vert sombre — hover, prix, liens texte */
    --secondary-color:#d4a574;  /* Beige/bois — accents chauds, flèches, détails */
    --dark-bg:        #2a2520;  /* Brun foncé — navbar, headers cartes, footer, hero */
    --dark-wood:      #3d3530;  /* Brun bois — gradient avec dark-bg */
    --light-bg:       #f8f7f5;  /* Blanc cassé — fonds de sections alternés */
    --text-dark:      #2a2520;  /* Corps principal sur fond clair */
    --text-light:     #ffffff;  /* Corps sur fond sombre */
    --text-gray:      #6b6b6b;  /* Texte secondaire, descriptions */
    --border-radius:  12px;     /* Rayon standard de toutes les cartes */
    --transition:     all 0.3s ease; /* Transition standard */
}
```

---

## 3. Typographie

**Police :** Poppins (Google Fonts) — weights 300 / 400 / 500 / 600 / 700

| Élément              | Taille    | Weight | Couleur         |
|----------------------|-----------|--------|-----------------|
| H1 hero              | 3rem      | 700    | text-light      |
| H2 section           | 2.5rem    | 700    | text-dark       |
| H3 carte             | 1.3–1.8rem| 600    | text-dark       |
| H4 processus/detail  | 1rem      | 600    | text-dark       |
| Sous-titre section   | 1.1rem    | 400    | text-gray       |
| Corps standard       | 1rem      | 400    | text-gray       |
| Corps lead (À propos)| 1.2rem    | 500    | primary-dark    |
| Tags / badges        | 0.85–0.9rem| 600   | variable        |
| Détail / disclaimer  | 0.82–0.85rem| 400  | text-gray       |

**Line-height :** 1.6 standard / 1.8 pour les corps longs / 1.6 pour les descriptions courtes.

---

## 4. Couleurs — Règles d'usage

| Couleur          | Usage autorisé                              | Interdit                        |
|------------------|---------------------------------------------|---------------------------------|
| primary (#7ed957)| CTA primaires, icônes SVG, puces ✓, badges  | Texte long, fonds de section    |
| primary-dark     | Hover sur primary, prix dans tarifs, liens  | CTA directement                 |
| secondary (#d4a574)| Flèches déco, sous-titres hero, accents   | Fonds de section, textes longs  |
| dark-bg          | Navbar, headers de cartes, footer, hero     | Corps de texte                  |
| light-bg (#f8f7f5)| Fonds de sections alternées, formulaires  | Cartes (utiliser white)         |
| white            | Fonds de cartes, cartes internes            | Sections entières (utiliser light-bg) |
| text-gray        | Descriptions, corps secondaire              | Titres, CTAs                    |

---

## 5. Alternance des backgrounds de sections

**RÈGLE ABSOLUE : Ne jamais avoir deux sections de même fond consécutives.**

```
Hero          → background: gradient dark-bg → dark-wood (+ image overlay 30%)
À propos      → background: light-bg
Services      → background: white
Réalisations  → background: white (interne: case-study-card sur light-bg)
Tarifs        → background: light-bg (cartes internes: white)
Contact       → background: white
Footer        → background: dark-bg
```

---

## 6. Structure des sections (OBLIGATOIRE)

Chaque section `<section>` doit suivre ce patron :

```html
<section id="[id]" class="[nom-section]">
    <div class="container">
        <div class="section-header">
            <h2>Titre de la section</h2>
            <div class="section-line"></div>
            <p class="section-subtitle">Sous-titre optionnel</p>  <!-- si besoin -->
        </div>
        <!-- contenu -->
    </div>
</section>
```

- `.section-header` : `margin-bottom: 60px`, `text-align: center`
- `.section-line` : 80px × 4px, `gradient(primary → secondary)`, centré
- Padding de section : `80px 20px` (desktop) / `60px 15px` (mobile 480px)

---

## 7. Composants

### Boutons
```
.btn-primary   → bg: primary / color: text-dark → action principale (1 par section max)
.btn-secondary → transparent / border: secondary → CTA secondaire (hero uniquement)
.btn-outline   → transparent / border: primary / color: primary → action tertiaire
```
- Padding : `15px 35px` / Border-radius : `var(--border-radius)` / Font-weight : 600
- Hover : `translateY(-2px)` + box-shadow

### Cards standard (.feature-card, .service-card, .tarif-card)
- Background : white (sur light-bg) ou light-bg (sur white)
- Border-radius : `var(--border-radius)`
- Box-shadow : `0 5px 20px rgba(0,0,0,0.05–0.08)`
- Hover : `transform: translateY(-5px)` + shadow amplifié
- Pas de border visible au repos (sauf `.featured` / `.tarif-card-featured`)

### .service-card (règles spécifiques)
```css
display: flex;
flex-direction: column;   /* OBLIGATOIRE pour que le CTA colle en bas */
padding: 40px 30px;
background: var(--light-bg);
```
- Icône : carré 70×70px, gradient primary → primary-dark, border-radius 15px
- `.service-cta` : `margin-top: auto` (pas `margin-top: 20px`)

### .tarif-card (règles spécifiques)
- Header : `gradient(dark-bg → dark-wood)` — cohérent avec navbar/footer
- Body : padding `20px 30px 30px`
- Options : séparées par `border-bottom: 1px solid #f0f0f0`
- Featured : `border: 2px solid primary`

### .cas-concret / Case Study
- Carte conteneur : `background: light-bg`, `padding: 30px`, grille `1fr auto 1fr`
- Colonnes : `background: white`, `border-radius: var(--border-radius)`, `padding: 30px`
- Colonne "Avant" : `border-left: 4px solid #e74c3c`
- Colonne "Après" : `border-left: 4px solid var(--primary-color)`
- Flèche : couleur `secondary`, centrée verticalement avec `align-self: center`

### .processus (bandeau 3 étapes)
- `display: flex`, `background: white`, `padding: 35px 40px`, `box-shadow` léger
- Numéros : cercle 42px, `background: primary`, centré
- Flèches : couleur `secondary`, `font-size: 1.4rem`
- Passe en colonne à 900px (pas 768px)

---

## 8. Animations

| Élément               | Animation       | Délai  |
|-----------------------|-----------------|--------|
| Hero logo             | fadeInDown      | 0s     |
| Hero title            | fadeInUp        | 0.2s   |
| Hero subtitle         | fadeInUp        | 0.4s   |
| Hero targets (tags)   | fadeInUp        | 0.5s   |
| Hero CTA              | fadeInUp        | 0.6s   |
| Cards au scroll       | opacity 0→1 via IntersectionObserver (script.js) |

- Transition globale : `all 0.3s ease` (var --transition)
- Hover sur cartes : `translateY(-5px)` uniquement

---

## 9. Breakpoints responsives

| Breakpoint | Règles principales |
|------------|-------------------|
| 1024px     | Nav gap réduit (18px), nav-link font 0.9rem |
| 900px      | .processus en colonne, .case-study-card en colonne |
| 768px      | Hamburger menu, grilles → 1 colonne, contact vertical |
| 480px      | Hero texte réduit, section padding 60px 15px |

---

## 10. Règles absolues — Ne jamais enfreindre

1. **Couleurs** : Utiliser exclusivement les CSS variables. Zéro valeur hexadécimale hardcodée.
2. **Fonds** : Respecter l'alternance light-bg / white entre sections.
3. **Service cards** : Toujours `display: flex; flex-direction: column` pour le CTA en bas.
4. **Section header** : Toujours h2 + `.section-line` dans chaque section.
5. **Animations de scroll** : Ne jamais supprimer l'IntersectionObserver du script.js.
6. **Breakpoints** : Ajouter le responsive AVANT de finir un composant (pas en option).
7. **CTA** : Un seul `.btn-primary` par section. Pas deux boutons verts côte à côte.
8. **Espacement** : Ne jamais cumuler `gap` (grid/flex) ET `margin-top` sur le même enfant.
9. **Nouveau composant** : Toujours créer son CSS dans styles.css avec un commentaire de section `/* ── Nom ─── */`.
10. **Suppression** : Avant de supprimer une section HTML, supprimer aussi ses classes CSS orphelines.
