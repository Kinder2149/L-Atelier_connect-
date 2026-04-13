# PROJET_CONTEXTE — L'Atelier Connecté

> Emplacement de ce fichier une fois rempli : racine du projet concerné
> Template source : METHODO/PROJET_CONTEXTE_TEMPLATE.md
>
> ⚠️ INSTRUCTION POUR L'IA (Claude et Cascade)
> Ce fichier est la source de vérité absolue du projet.
> Le lire EN ENTIER avant toute action.
> Toute décision technique qui le contredit est interdite.
> Si une demande sort de ce cadre : poser UNE question avant d'agir.

---

## 1. IDENTITÉ DU PROJET

| Champ | Valeur |
|---|---|
| Nom | L'Atelier Connecté |
| Type | Web |
| Objectif en 1 phrase | Présenter l'offre de services numériques locaux et générer des prises de contact via un formulaire. |
| Statut | ⚠️ À confirmer (En développement / En production) |
| Utilisateurs actuels | ⚠️ À confirmer |
| Dernière mise à jour de ce fichier | 2026-04-13 |

---

## 2. STACK TECHNIQUE

> Tout ce qui n'est pas listé ici ne doit pas être utilisé sans validation.

**Frontend :**
- Framework : Aucun framework (site statique)
- Langage : HTML5, CSS3, JavaScript
- Composants UI : Sections vitrine (Accueil, À propos, Services, Cas concret, Tarifs, Contact)
- Gestion de l'affichage dynamique : JavaScript DOM (menu mobile, scroll smooth, animations IntersectionObserver, gestion formulaire)

**Backend :**
- Framework : Aucun
- Langage : Aucun
- Port local : N/A (prévisualisation via serveur statique IDE)

**Base de données :**
- Technologie : Aucune
- Outil de liaison avec le code : Aucun
- Lancement en local : N/A

**Services externes :**
- Comptes utilisateurs : Aucun
- Stockage fichiers : Fichiers locaux (`assets/`)
- Mise en ligne : GitHub Pages (documenté dans `README.md`)
- Autres : EmailJS (envoi formulaire), Google Fonts, CDN jsDelivr (lib EmailJS)

---

## 3. ARCHITECTURE

> Cette structure ne change pas sans validation écrite dans ce fichier.

```
L-Atelier_connect-/
├── index.html
├── styles.css
├── script.js
├── PROJET_CONTEXTE.md
├── README.md
├── STACK_STANDARD.md
├── _archives/
│   ├── GUIDE-EMAILJS.md
│   ├── PROJET_CONTEXTE_TEMPLATE.md
│   ├── README_METHODE.md
│   └── ressources/
│       ├── BASE DE SPEECH – Porte à porte ...md
│       ├── DESIGN_SYSTEM.md
│       ├── DOCUMENT DE PRÉSENTATION ...md
│       ├── Document de cadrage stratégique perso ...md
│       └── PROMPT_CASCADE_REFONTE.md
├── assets/
│   ├── Logo base.jpeg
│   ├── base 1 .png
│   ├── fond 1.jpg
│   ├── fond 2.jpg
│   ├── instagram.png
│   ├── logo simple.png
│   └── titre clair.png
├── ressources/
├── emailjs-template.html
└── template-reponse-gmail.html
```

**Nombre de services actifs :** 3 / 20 maximum

---

## 4. FONCTIONNALITÉS

### ✅ Stables (ne pas toucher sans raison)
- Navigation responsive avec menu mobile et liens d'ancrage.
- Page vitrine complète avec sections marketing.
- Formulaire de contact connecté à EmailJS.
- Animations d'apparition au scroll.

### 🚧 En cours (mission actuelle uniquement)
- Reprise projet existant : création du contexte projet et alignement documentaire.

### ❌ Bugs connus
- ⚠️ À confirmer (aucun bug formalisé dans la documentation actuelle).

### 🔒 Hors scope (ne jamais implémenter sans décision explicite)
- Ajout d'un backend ou d'une base de données.
- Refonte visuelle majeure du site.
- Ajout de nouvelles dépendances tierces.

---

## 5. RÈGLES STRICTES DU PROJET

- Ne modifier QUE les fichiers concernés par la mission en cours.
- Ne créer aucun nouveau fichier sans le lister ici après création.
- Ne pas ajouter de dépendance sans demande explicite.
- Modifier l'existant avant d'en créer du nouveau.
- Zéro structure vide créée "pour le futur".
- Pendant la reprise P2 : aucune suppression définitive, aucun refactoring, aucune modification de code applicatif.

---

## 6. DÉCISIONS FIGÉES

> Ces décisions ont été prises et validées. Elles ne se remettent pas en question.

| Date | Décision | Raison |
|---|---|---|
| ⚠️ À confirmer | Le site reste une application statique sans backend. | Simplicité de maintenance et coût réduit. |
| ⚠️ À confirmer | Le formulaire de contact utilise EmailJS côté client. | Éviter la mise en place d'un serveur d'envoi. |
| ⚠️ À confirmer | Les visuels sont stockés localement dans `assets/`. | Déploiement simple sur hébergement statique. |

---

## 7. FICHIERS DE DOCUMENTATION AUTORISÉS

| Fichier | Rôle |
|---|---|
| PROJET_CONTEXTE.md | Source de vérité (ce fichier) |
| CHANGELOG.md | Historique des missions terminées |
| BUGS.md | Bugs connus et leur statut |
| README.md | Présentation du projet |
| STACK_STANDARD.md | Stack de référence |

Tout autre fichier `.md` va dans `_archives/`.

---

## 8. SESSION EN COURS

> Remplir EN DÉBUT de session. Compléter EN FIN de session.

**Objectif de la session :** Nettoyage visuel section cas concret, correction bug JS animation, intégration normes design, suppression fichiers parasites.  
**Fichiers concernés :** `index.html`, `styles.css`, `script.js`, `PROJET_CONTEXTE.md`, `_archives/ressources/`.  
**Hors scope cette session :** sections `hero`, `apropos`, `services`, `tarifs`, `contact`, `footer`, navigation, EmailJS hors ligne 43, `README.md`, `STACK_STANDARD.md`, `assets/`.  
**Résultat de fin de session :** ⚠️ En cours.

---

## 9. BACKLOG (missions suivantes)

> Ordonné par priorité. Ne jamais commencer la suivante sans que la précédente soit ✅ testée.

1. Valider et compléter les champs marqués `⚠️ À confirmer`.
2. Finaliser la reprise P2 (archivage docs + vérification structure + alignement validé).
3. Formaliser les bugs connus dans `BUGS.md` si nécessaire après test manuel.

---

## 10. NORMES DE DESIGN

### Palette (variables CSS source)

- `--primary-color` : `#7ed957`
- `--primary-dark` : `#5fb83a`
- `--secondary-color` : `#d4a574`
- `--dark-bg` : `#2a2520`
- `--dark-wood` : `#3d3530`
- `--light-bg` : `#f8f7f5`
- `--text-dark` : `#2a2520`
- `--text-light` : `#ffffff`
- `--text-gray` : `#6b6b6b`

### Typographie

- Police unique projet : `Poppins`, sans-serif.
- Tailles repères :
  - Titres section (`h2`) : `2.5rem`
  - Titre hero (`h1`) : `3rem`
  - Sous-titres section : `1.1rem`
  - Texte courant : `1rem` (line-height global `1.6`)
  - Micro-textes/badges/disclaimer : `0.82rem` à `0.95rem`
- Graisses utilisées : `300`, `400`, `500`, `600`, `700`.

### Espacements

- Padding standard des sections : `80px 20px` (mobile `60px 15px`).
- Largeur conteneur : `max-width: 1200px`, padding latéral `20px`.
- Gaps usuels des grilles : `20px`, `24px`, `30px` selon densité du bloc.
- Rayon standard composants : `--border-radius` (`12px`).

### Règles composants

- Cartes : fond défini (`white` ou `var(--light-bg)`), coins arrondis, ombre légère, transition homogène (`--transition`).
- Boutons : `.btn` base commune, variantes `.btn-primary` / `.btn-secondary`, état hover systématique.
- Badges/résultats : texte court, lisible en un coup d'œil, contraste suffisant, usage prioritaire des variables existantes.
- Cas concret : structure `Avant / Après` en grille conservée, disclaimer maintenu si illustration fictive.

### Règles strictes

- Ne jamais créer de nouvelle variable CSS sans validation explicite.
- Ne jamais laisser une section sans fond défini.
- Ne jamais ajouter de placeholder vide.
- Ne jamais casser l'alignement vertical/horizontal des cartes entre desktop et mobile.
- Améliorer l'existant sans refonte globale non demandée.

---

*Template source : METHODO/PROJET_CONTEXTE_TEMPLATE.md*  
*Rempli avec : Cascade (analyse projet existant)*  
*Lu par : Cascade à chaque début de session*
