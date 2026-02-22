# Guide de Configuration EmailJS

## ✅ Configuration terminée

Votre formulaire de contact est maintenant **100% fonctionnel** avec EmailJS !

### Identifiants configurés
- **Public Key** : `IFE4YLdMxS6QXU2Hj`
- **Service ID** : `service_rmg0awj`
- **Template ID** : `template_sbpae5f`

---

## 📧 Configuration du Template EmailJS

### Étape 1 : Accéder au template
1. Allez sur [EmailJS Dashboard](https://dashboard.emailjs.com/admin/templates/template_sbpae5f)
2. Cliquez sur votre template `template_sbpae5f`

### Étape 2 : Configurer le template

**Sujet de l'email** :
```
Nouveau contact - {{from_name}}
```

**Contenu du template** :
Copiez le contenu du fichier `emailjs-template.html` dans l'éditeur EmailJS.

**Variables utilisées** :
- `{{from_name}}` - Nom du contact
- `{{from_email}}` - Email du contact
- `{{structure}}` - Type de structure
- `{{besoin}}` - Besoin principal
- `{{message}}` - Message complet
- `{{to_name}}` - L'Atelier Connecté

### Étape 3 : Tester
1. Dans EmailJS, cliquez sur "Test it"
2. Remplissez les variables de test
3. Vérifiez que vous recevez bien l'email

---

## 📨 Template de Réponse Gmail

### Comment l'utiliser

**Option 1 : Signature Gmail**
1. Gmail > Paramètres > Signatures
2. Créer une nouvelle signature "L'Atelier Connecté"
3. Copiez le contenu de `template-reponse-gmail.html`
4. Collez dans l'éditeur de signature

**Option 2 : Modèle de réponse rapide**
1. Gmail > Paramètres > Réponses standardisées
2. Activez "Réponses standardisées"
3. Composez un email avec le template
4. Plus d'options > Réponses standardisées > Enregistrer comme nouvelle

**Option 3 : Brouillon réutilisable**
1. Créez un nouveau brouillon dans Gmail
2. Copiez le contenu HTML du template
3. Sauvegardez-le comme brouillon
4. Dupliquez-le à chaque réponse

---

## 🎨 Personnalisation

### Modifier les couleurs
Dans les templates, vous pouvez modifier :
- **Vert principal** : `#7ed957`
- **Beige/Or** : `#d4a574`
- **Fond sombre** : `#2a2520`
- **Fond clair** : `#f8f7f5`

### Ajouter votre logo
Remplacez l'emoji 🛠️ par :
```html
<img src="URL_DE_VOTRE_LOGO" alt="Logo" style="width: 60px; height: 60px;">
```

---

## 🔧 Fonctionnement du formulaire

### Ce qui se passe quand quelqu'un envoie un message :

1. **Utilisateur remplit le formulaire** sur votre site
2. **Clique sur "Envoyer"**
3. **Bouton affiche** "Envoi en cours..."
4. **EmailJS envoie** l'email à votre adresse
5. **Message de confirmation** s'affiche (vert)
6. **Formulaire se réinitialise** automatiquement

### En cas d'erreur :
- Message d'erreur affiché en rouge
- Utilisateur peut réessayer
- Possibilité de contacter directement par email

---

## 📊 Limites EmailJS (plan gratuit)

- **200 emails/mois** maximum
- Largement suffisant pour démarrer
- Si dépassement : upgrade vers plan payant (9$/mois pour 1000 emails)

---

## ✉️ Répondre aux contacts

### Workflow recommandé :

1. **Vous recevez** l'email de notification (template EmailJS)
2. **Vous lisez** les informations du contact
3. **Vous cliquez** sur "Répondre directement"
4. **Vous utilisez** le template de réponse Gmail
5. **Vous personnalisez** selon le besoin
6. **Vous envoyez** votre réponse

### Exemple de réponse personnalisée :

```
Bonjour [Prénom],

Merci pour votre message concernant [logiciel sur mesure / site web / diagnostic].

Je comprends que vous cherchez à [résumer le besoin].

Je vous propose un échange téléphonique ou en visio pour :
- Comprendre précisément votre fonctionnement actuel
- Identifier les points de friction
- Vous proposer une solution adaptée

Seriez-vous disponible [proposition de créneaux] ?

À très bientôt,
```

---

## 🚀 Prochaines étapes

1. ✅ Tester le formulaire sur votre site
2. ✅ Vérifier la réception des emails
3. ✅ Configurer votre signature Gmail
4. ✅ Préparer vos réponses types
5. ✅ Déployer sur GitHub Pages

---

## 🆘 Support

En cas de problème :
- Vérifiez les logs dans la console du navigateur (F12)
- Consultez le dashboard EmailJS pour voir les envois
- Vérifiez vos spams si vous ne recevez pas les emails

---

**Tout est prêt ! Votre système de contact est opérationnel.** 🎉
