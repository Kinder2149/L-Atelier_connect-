# Prompt Cascade — L'Atelier Connecté
> À utiliser dans une nouvelle session IA pour intervenir proprement sur ce projet.
> Copie-colle le prompt correspondant à la tâche voulue.

---

## PROMPT 0 — Briefing projet (à envoyer EN PREMIER dans toute nouvelle session)

```
Tu vas travailler sur le site "L'Atelier Connecté", micro-entreprise d'artisanat
numérique local basée à Villeurbanne (Lyon, France).

## Structure du projet
Répertoire : /home/user/L-Atelier_connect-/
Fichiers principaux :
- index.html          → page unique, toutes les sections
- styles.css          → toutes les règles CSS, aucun framework
- script.js           → navigation mobile + IntersectionObserver + EmailJS
- assets/             → images (logo, fonds, instagram.png)
- ressources/         → documents stratégiques (NE PAS MODIFIER)

## Design System
Avant toute intervention, lis OBLIGATOIREMENT le fichier :
ressources/DESIGN_SYSTEM.md

Ce fichier définit les règles absolues de design. Toute modification doit les respecter.

## Palette principale
- Vert action : #7ed957 (--primary-color)
- Vert hover  : #5fb83a (--primary-dark)
- Beige bois  : #d4a574 (--secondary-color)
- Fond sombre : #2a2520 (--dark-bg)
- Fond bois   : #3d3530 (--dark-wood)
- Fond clair  : #f8f7f5 (--light-bg)

## Structure des sections dans index.html (dans l'ordre)
1. navbar        → fixe, dark-bg, 6 liens
2. #accueil      → hero plein écran, dark gradient + image overlay
3. #apropos      → light-bg, texte + 3 feature-cards
4. #services     → white, 3 service-cards en flex colonne
5. #realisations → white, case-study avant/après
6. #tarifs       → light-bg, processus 3 étapes + grille tarifs + offre lancement
7. #contact      → white, info gauche + formulaire droite
8. footer        → dark-bg, 3 colonnes

## Règles de workflow
- Lire le fichier AVANT de le modifier
- Respecter l'alternance des fonds de sections
- Tester le responsive (breakpoints : 1024px, 900px, 768px, 480px)
- Committer avec un message descriptif après chaque modification significative
```

---

## PROMPT 1 — Corriger un bug de design CSS

```
Tu dois corriger des bugs visuels sur le site L'Atelier Connecté.
Lis d'abord ressources/DESIGN_SYSTEM.md, puis index.html et styles.css en entier.

Bugs à corriger (liste exhaustive, dans l'ordre) :

[REMPLACE CE BLOC PAR LA LISTE DE BUGS]
Exemple :
- Section #services : les cards n'ont pas la même hauteur car .service-card
  manque de display:flex + flex-direction:column
- Section #realisations : les colonnes avant/après n'ont pas de fond blanc
  ni de bordure colorée gauche

Pour chaque bug :
1. Identifie la règle CSS ou la structure HTML responsable
2. Applique le correctif minimal (ne touche pas à ce qui fonctionne)
3. Vérifie que le correctif respecte le DESIGN_SYSTEM.md
4. Teste mentalement le résultat sur desktop ET mobile

Après les corrections, committe avec un message clair.
```

---

## PROMPT 2 — Ajouter une nouvelle section

```
Tu dois ajouter une nouvelle section au site L'Atelier Connecté.
Lis d'abord ressources/DESIGN_SYSTEM.md, puis index.html et styles.css en entier.

Section à créer : [NOM DE LA SECTION]
Emplacement dans la page : après la section [SECTION PRÉCÉDENTE]
Contenu : [DÉCRIRE LE CONTENU]
Fond : [white OU light-bg — respecter l'alternance du DESIGN_SYSTEM]

Règles impératives :
1. La section doit avoir un id unique et une classe CSS unique
2. Utiliser la structure section-header standard (h2 + .section-line + p.section-subtitle)
3. Utiliser exclusivement les CSS variables du design system
4. Ajouter un lien dans la navbar ET dans le footer
5. Créer les styles CSS avec un commentaire de section /* ── Nom ─── */
6. Ajouter les règles responsive (1024px, 900px, 768px, 480px si nécessaire)
7. Committer après création

Ne jamais :
- Coder des couleurs hex directement dans le CSS
- Oublier le responsive
- Créer deux sections consécutives de même fond
```

---

## PROMPT 3 — Intégrer un projet réel dans "Réalisations"

```
Tu dois remplacer le cas concret fictif de la section #realisations par un 
projet réel dans le site L'Atelier Connecté.
Lis d'abord ressources/DESIGN_SYSTEM.md, puis la section #realisations dans index.html.

Données du projet réel :
- Nom/type du client : [EX: Coiffeur de quartier, Villeurbanne]
- Situation AVANT : [liste des problèmes]
- Solution apportée : [liste de ce qui a été fait]
- Résultats mesurables : [ex: 0 double réservation, visible sur Google, etc.]
- Durée d'intervention : [ex: 2 semaines]

Instructions :
1. Remplace le contenu des deux .case-study-col (avant / après)
2. Mets à jour les .case-results avec les vrais résultats
3. Supprime la balise .case-disclaimer si le projet est réel (elle sert uniquement
   pour les illustrations fictives)
4. Si plusieurs projets disponibles : crée un système de tabs ou de carousel
   en respectant le design system
5. Committer après modification
```

---

## PROMPT 4 — Mise à jour des tarifs

```
Tu dois mettre à jour les tarifs dans la section #tarifs du site L'Atelier Connecté.
Lis d'abord styles.css pour comprendre les classes .tarif-card, .tarif-option, etc.

Nouveaux tarifs à appliquer :
[DÉCRIRE ICI LES NOUVEAUX TARIFS]

Règles :
1. Ne modifier que les valeurs dans index.html (pas le CSS)
2. Structure d'un tarif-option :
   <div class="tarif-option">
     <div class="tarif-option-top">
       <span class="tarif-name">NOM</span>
       <span class="tarif-price">à partir de <strong>XXX €</strong></span>
     </div>
     <span class="tarif-detail">Description courte</span>
   </div>
3. Pour "Devis gratuit" : <span class="tarif-price"><strong>Devis gratuit</strong></span>
4. Mettre à jour aussi l'offre de lancement si les conditions changent
5. Committer après modification
```

---

## PROMPT 5 — Audit complet avant mise en ligne

```
Effectue un audit complet du site L'Atelier Connecté avant déploiement.
Lis ressources/DESIGN_SYSTEM.md, puis index.html et styles.css en entier.

Vérifie dans l'ordre :

DESIGN
□ Alternance des fonds de sections respectée (light-bg / white)
□ Toutes les sections ont section-header + section-line
□ Aucune couleur hex hardcodée dans styles.css
□ Les service-cards ont display:flex + flex-direction:column
□ Les CTA sont cohérents (un seul btn-primary par section)

CONTENU
□ Copyright à jour (année courante)
□ Email contact fonctionnel (atelierconnecte.contact@gmail.com)
□ Lien Instagram correct (@keamder_dev)
□ Zone d'intervention à jour (Villeurbanne 69100)
□ Cas concret : disclaimer présent si illustration fictive, absent si réel
□ Offre de lancement : toujours valide ? (5 premiers clients)

TECHNIQUE  
□ Tous les liens internes fonctionnent (#accueil, #apropos, etc.)
□ Le formulaire de contact a les bons IDs EmailJS (script.js)
□ Les images existent dans assets/ (logo simple.png, Logo base.jpeg, etc.)
□ Les animations IntersectionObserver sont intactes dans script.js
□ Aucune classe CSS orpheline (classes définies mais non utilisées)

RESPONSIVE
□ Navigation mobile (hamburger) fonctionne à 768px
□ Les grilles passent en 1 colonne à 768px
□ Le processus passe en colonne à 900px
□ Le case-study passe en colonne à 900px
□ La navbar ne déborde pas à 1024px (6 items)

Pour chaque problème trouvé : signale-le avec le fichier + numéro de ligne.
Ne modifie rien pendant l'audit — rapport uniquement.
```

---

## PROMPT 6 — Déploiement GitHub Pages

```
Tu dois préparer et déployer le site L'Atelier Connecté sur GitHub Pages.

Étapes dans l'ordre :
1. Vérifie le statut git (git status)
2. S'il y a des fichiers non commités : identifie-les et demande confirmation
3. Vérifie que tu es sur la bonne branche (main)
4. Pousse vers origin main : git push -u origin main
5. Confirme que GitHub Pages est configuré sur la branche main
   (Settings > Pages > Source: Deploy from branch > main > / root)

URL du site après déploiement : https://kinder2149.github.io/L-Atelier_connect-/

En cas d'erreur de push : réessaie jusqu'à 4 fois avec délai croissant (2s, 4s, 8s, 16s).
Ne jamais force-push sur main.
```
