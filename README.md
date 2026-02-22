# L'atelier connecté

Site web professionnel pour L'atelier connecté - Accompagnement des associations dans leur transition numérique.

## 🚀 Déploiement sur GitHub Pages

### Étapes pour publier le site :

1. **Créer un dépôt GitHub**
   - Allez sur [GitHub](https://github.com) et créez un nouveau dépôt
   - Nommez-le `atelier-connecte` (ou le nom de votre choix)
   - Ne cochez pas "Initialize with README"

2. **Pousser le code vers GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Site L'atelier connecté"
   git branch -M main
   git remote add origin https://github.com/VOTRE-USERNAME/atelier-connecte.git
   git push -u origin main
   ```

3. **Activer GitHub Pages**
   - Dans votre dépôt GitHub, allez dans `Settings` > `Pages`
   - Source : sélectionnez `main` branch
   - Folder : sélectionnez `/ (root)`
   - Cliquez sur `Save`
   - Votre site sera disponible à : `https://VOTRE-USERNAME.github.io/atelier-connecte/`

## 📱 Caractéristiques

- ✅ Design **mobile-first** responsive
- ✅ Navigation fluide avec menu hamburger mobile
- ✅ Animations et transitions modernes
- ✅ Formulaire de contact interactif
- ✅ Optimisé pour tous les appareils
- ✅ Performance optimale
- ✅ SEO-friendly

## 🎨 Sections

1. **Hero** - Page d'accueil avec logo et appel à l'action
2. **À propos** - Présentation de la mission et des valeurs
3. **Services** - Détail des services proposés
4. **Forfaits** - Packages avec tarification
5. **Contact** - Formulaire et coordonnées

## 🛠️ Technologies

- HTML5
- CSS3 (avec variables CSS et animations)
- JavaScript vanilla (pas de dépendances)
- Google Fonts (Poppins)

## 📝 Personnalisation

### Modifier les coordonnées de contact

Éditez le fichier `index.html` dans la section `#contact` :
- Email : ligne avec `mailto:`
- Téléphone : ligne avec `tel:`
- Localisation : texte de localisation

### Modifier les couleurs

Éditez les variables CSS dans `styles.css` (lignes 1-10) :
```css
:root {
    --primary-color: #7ed957;
    --secondary-color: #d4a574;
    /* ... */
}
```

### Ajouter vos liens réseaux sociaux

Éditez le footer dans `index.html` et remplacez les `href="#"` par vos vraies URLs.

## 📧 Formulaire de contact

Le formulaire est actuellement configuré pour afficher une alerte. Pour le connecter à un service d'envoi d'emails :

**Options recommandées :**
- [Formspree](https://formspree.io/) - Gratuit jusqu'à 50 soumissions/mois
- [EmailJS](https://www.emailjs.com/) - Gratuit jusqu'à 200 emails/mois
- [Netlify Forms](https://www.netlify.com/products/forms/) - Si hébergé sur Netlify

## 🎯 Prochaines étapes

1. Remplacer les coordonnées de contact par les vraies
2. Ajouter les liens vers vos réseaux sociaux
3. Configurer le formulaire de contact avec un service d'envoi
4. Ajouter Google Analytics (optionnel)
5. Configurer un nom de domaine personnalisé (optionnel)

## 📄 Structure des fichiers

```
atelier-connecte/
├── index.html          # Page principale
├── styles.css          # Styles CSS
├── script.js           # JavaScript
├── README.md           # Documentation
└── assets/             # Images et ressources
    ├── Logo base.jpeg
    ├── logo simple.png
    ├── titre clair.png
    ├── base 1 .png
    ├── fond 1.jpg
    └── fond 2.jpg
```

## 💡 Support

Pour toute question ou modification, consultez la documentation ou contactez le développeur.

---

© 2024 L'atelier connecté. Tous droits réservés.
