# Formation CSS Eirbware - Enseirb-MATMECA

## Introduction
CSS (Cascading Style Sheets ou Feuilles de style en cascade) est un langage de description des docs HTML/XML, créé en 1996.

Dernier standard défini par la W3C : CSS "4", avec des modules indépendant mis à jour fréquemment.

Fonctionne sur un système de sélecteurs (elements, IDs, classes) pour styliser la page web.

## Comment écrire du CSS ?

### Fonctionnement de base
```css
selecteur {
    propriete1: valeur1;
    propriete2: valeur2;
}
```
### 3 possibilités
* Dans un fichier .css séparé du HTML :
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <link rel="stylesheet" href="style.css" />
        <title>Exemple</title>
    </head>
    <body>
        ...
    </body>
</html>
```
* Dans l'en tête du fichier HTML :
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            p {
                color: blue;
            }
        </style>
        <title>Exemple</title>
    </head>
    <body>
        ...
    </body>
</html>
```
* A l'intérieur d'une balise HTML :
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>Exemple</title>
    </head>
    <body>
        <p style="color: blue;">Enseirb &gt; Enscbp</p>
    </body>
</html>
```

### Sélecteurs
* Elements
```css
p {
    color: blue; /* Les paragraphes seront en bleu */
}
```

* IDs
```css
#mytext {
    color: blue; /* Les IDs mytext seront en bleu */
}
```

* Classes
```css
.mytext {
    color: blue; /* Les classes mytext seront en bleu */
}
```

* Pseudo-classes
  * Survol de la souris
  ```css
  a:hover {
      color: green; /* Les liens seront en vert lors du survol */
  }
  ```
  * Clic de la souris
  ```css
  p:active {
      color: red; /* Les paragraphes seront en rouge lors du clic */
  }
  ```
  * Lien déjà visité
  ```css
  a:visited {
      color: orange; /* Les liens visités seront en orange */
  }
  ```
  * Element actif
  ```css
  input[type=text]:focus {
      background-color: pink; /* Les champs de texte seront en rose lorsque la saisie est active */
  }
  ```
  * Premier / dernier élément
  ```css
  div:first-child {
      text-align: center; /* Les premiers enfants des divs seront centrés */
  }
  ```
  ```css
  div:last-child {
      text-align: center; /* Les derniers enfants des divs seront centrés */
  }
  ```

* Autres sélecteurs : https://www.w3schools.com/cssref/css_selectors.asp ou https://www.w3.org/Style/css3-selectors-updates/WD-css3-selectors-20010126.fr.html#selectors

### Propriétés communes
#### Texte
* ```font-size: 12px;``` : taille du texte (en %, px ou em)
  * https://www.w3schools.com/cssref/pr_font_font-size.asp
* ```font-family: police;``` : police
  * https://www.w3schools.com/cssref/pr_font_font-family.asp
  * Polices pour le web : https://www.w3schools.com/cssref/css_websafe_fonts.asp
* ```font-style: italic;``` : style du texte (normal, italic, oblique)
  * https://www.w3schools.com/cssref/pr_font_font-style.asp
* ```font-weight: bold;``` : style du texte (normal, bold)
  * https://www.w3schools.com/cssref/pr_font_weight.asp
* ```font-align: center;``` : alignement du texte (left, center, right, justify)
  * https://www.w3schools.com/cssref/pr_text_text-align.ASP
* ```color: blue;``` : couleur du texte (nom de la couleur, rgb(0, 0, 0), #rrggbb)
  * https://www.w3schools.com/cssref/pr_text_color.asp
  * taper 'color picker' sur Google
  * Couleurs dans la norme CSS : https://www.w3schools.com/cssref/css_colors.asp

#### Fond
* ```background-color: blue;``` : couleur de fond (nom de la couleur, rgb(0, 0, 0), #rrggbb)
  * https://www.w3schools.com/csSref/pr_background-color.asp
* ```background-image: url("logo.jpg");``` : image de fond
  * https://www.w3schools.com/cssref/pr_background-image.asp
* ```background-attachment: fixed;``` : défilement de l'image de fond (fixed, scroll)
  * https://www.w3schools.com/cssref/pr_background-attachment.asp
* ```background-repeat: no-repeat;``` : répétition de l'image de fond (no-repeat, repeat-x, repeat-y, repeat)
  * https://www.w3schools.com/cssref/pr_background-repeat.asp
* ```background-position: top right;``` : position de l'image de fond (top, bottom, left, center, right)
  * https://www.w3schools.com/cssref/pr_background-position.asp

#### Bordures
* ```border: 3px blue dashed;``` (largeur / couleur / motif)
* (et ```border-top```, ```border-bottom```, ```border-left```, ```border-right```)
  * https://www.w3schools.com/cssref/pr_border.asp
* ```border-radius: 10px;``` : arrondi de la bordure
  * https://www.w3schools.com/cssref/css3_pr_border-radius.asp

#### Blocs et positionnement
* ```width: 640px;``` : largeur (en px ou %)
  * https://www.w3schools.com/css/css_dimension.asp
* ```height: 480px;``` : hauteur (en px ou %)
  * https://www.w3schools.com/css/css_dimension.asp
* ```padding: 12px;``` ou ```padding: 12px 20px;``` ou ```padding: 12px 20px 12px 15px;```: marge intérieure
* ```margin: 50px;``` ou ```margin: 50px 25px;``` ou ```margin: 50px 25px 30px 20px;``` : marge extérieure
  * https://www.w3schools.com/css/css_margin.asp
* ```position: absolute;``` : position de l'élément (static, absolute, relative, fixed, sticky)
* ```top: 80px;```, ```bottom: 80px;```, ```left: 80px;```, ```right: 80px;``` : position par rapport à la propriété ```position``` (en px ou %)
  * https://www.w3schools.com/css/css_positioning.asp

## Liens utiles
* W3Schools (référence CSS) : https://www.w3schools.com/css/
* MDN Web Docs (référence CSS) : https://developer.mozilla.org/fr/docs/Web/CSS
* W3C (standard CSS) : http://www.stylesheets.fr/Style/
* Caniuse (compatibilité propriétés CSS selon les navigateurs) : https://www.caniuse.com/
* Bootstrap (bibliothèque HTML/CSS/JS) : https://getbootstrap.com/
* MOOC OpenClassrooms : https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3
