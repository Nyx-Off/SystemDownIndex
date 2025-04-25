# SystemDown

## Page de maintenance rétro ASCII-art

![Version](https://img.shields.io/badge/version-1.0.0-green)
![License](https://img.shields.io/badge/license-MIT-blue)

**SystemDown** est une page de maintenance au style rétro inspirée des terminaux DOS et BBS des années 80-90. Elle utilise l'art ASCII et des effets visuels vintage pour informer les utilisateurs de manière engageante que votre site est temporairement indisponible.

![Preview](https://via.placeholder.com/800x400?text=SystemDown+Preview)

## Caractéristiques

- **Design ASCII Art** : Logo et séparateurs en art ASCII pur
- **Effets CRT authentiques** : Lignes de scan, clignotements aléatoires et effet de statique
- **Animations rétro** : Curseur clignotant, effet machine à écrire et barre de progression
- **Responsive** : S'adapte aux mobiles et tablettes
- **Poids léger** : Moins de 15ko, aucune dépendance JavaScript externe
- **Personnalisable** : Facile à modifier pour l'adapter à votre marque

## Installation

1. Téléchargez les fichiers `index.html` et `static.png`
2. Placez-les à la racine de votre serveur web
3. Configurez votre serveur pour rediriger vers cette page pendant la maintenance

```bash
# Exemple avec Apache (.htaccess)
RewriteEngine On
RewriteCond %{REMOTE_ADDR} !^123\.456\.789\.000
RewriteCond %{REQUEST_URI} !^/index\.html$
RewriteCond %{REQUEST_URI} !^/static\.png$
RewriteRule ^(.*)$ /index.html [R=503,L]
```

## Personnalisation

### Modification du texte
Ouvrez `index.html` et modifiez les sections suivantes :

- Titre : Balise `<title>` et `<h1 class="typewriter">`
- Messages : À l'intérieur des balises `<div class="warning">` et `<div class="status-window">`
- Pied de page : Dans `<div class="footer">`

### Modification de l'art ASCII
L'art ASCII se trouve dans les balises `<pre>`. Vous pouvez générer votre propre art ASCII avec des outils comme [ASCII Art Generator](https://www.asciiart.eu/text-to-ascii-art) et remplacer le contenu existant.

### Modification des couleurs
Modifiez les variables CSS au début du fichier pour changer le schéma de couleurs :

```css
:root {
    --main-green: #00ff00; /* Couleur principale du texte */
    --dark-green: #006600; /* Couleur secondaire */
    --background: #000000; /* Arrière-plan */
    --text-shadow: 0 0 5px rgba(0, 255, 0, 0.7); /* Ombre du texte */
    --scan-line-color: rgba(0, 20, 0, 0.2); /* Couleur des lignes de scan */
}
```

## Compatibilité

- Chrome 49+
- Firefox 45+
- Safari 9+
- Edge 12+
- Opera 36+

## Licence

Ce projet est sous licence MIT. Vous êtes libre de l'utiliser, le modifier et le distribuer comme bon vous semble.

## Crédits

- Police VT323 par [Google Fonts](https://fonts.google.com/specimen/VT323)
- Inspiré par l'esthétique des BBS, DOS et terminaux Unix des années 80-90
- Développé par [Votre nom]

---

*"En cas de dysfonctionnement, éteignez et rallumez."*
