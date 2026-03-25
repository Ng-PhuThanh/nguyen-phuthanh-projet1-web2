
# DOCUMENTATION.md

## 1. Système de nomenclature CSS

BME (Block Element Modifier) est une manière de structurer et d'améliorer la comprehension des classes HTML et CSS pour nous et pour les autres. Il donne tout les information a une instant sans avoir de la confusion, spécifique et une variation.

EXEMPLES :
- .navbar__link-item (Block principal)
- .hero__btn--secondary (Élément)
- .navbar (Variante)

ADVANTAGES : 
- Une meilleure lisibilité du code
- Une sépération claire des responsabilités
- Une réutilisation faciles des composantes
- Éviter les conflits de styles

## 2. Variables CSS et design tokens

Les variables sont définies dans :root pour centraliser le design system. C'une moyen pour permet de faciliter le déplacement et de maintenir une code simplifié au long du projet pour éviter d'avoire une répétition du meme code.

EXEMPLES : 
:root {
  --color-primary: #15133C;
  --color-secondary: #F1EEE9;
  --color-accent: #EC994B;

  --space-1: 4px;
  --space-2: 8px;
  --space-4: 16px;

  --font-size-base: 16px;
  --font-size-xl: 40px;

  --radius-md: 8px;
}

- Couleurs
- Espacements
- Typographies
- Rayons

EXEMPLS :
  VARIANTES :
- bouton primaire (.hero__btn--primary)
- bouton secondaire (.hero__btn--secondary)

ADVANTAGES :
- Changement rapide du design
- Cohérance sur tout le projet
- Maintenance facile
- Éviter des codes non nécessaires
- Moins de répétitions

## 3. Liste des composants réutilisables

Le projet est structuré en composants modulaires :

Utilisation des plusieurs composantes réutilisables pour que chaque composant possède leur propre bloc de CSS, sa structure HTML et ses éléments internes.

EXEMPLES :
- Navbar (.navbar)
- Hero (.hero)
- About (.about)
- Services (.services)
- Schedule (.schedule)
- Reviews (.reviews)
- Team (.team)
- Pricing (.pricing)
- Contact (.contact)
- Footer (.footer)

## 4. Décisions Flexbox pour les layouts complexes

Flexbox est la base principale pour permet tout les sections de s'adapter a une dimension donnée par le controle d'allignment, la distribution de l'espace et le comportement responsive. Les exemples sont ceux que j'ai utiliser le plus pour faire mon site web adpative.

EXEMPLES : 
- DISPLAY 
  - FLEX
- FLEX DIRECTION
  - COLUMN
  - ROW
- JUSTIFY-CONTENT
  - SPACE-BETWEEN
  - SPACE-AROUND
  - CENTER
- ALIGN-ITEMS
  - CENTER
  - LEFT
  - STRETCH
- ALIGN-SELF
  - CENTER
  - STRETCH
  - FLEX-START

.services {
  background: var(--color-primary, #15133C);;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  align-self: stretch;
  padding: 60px calc(20px + 8vw);
  gap: 60px;
}


ADVANTAGES :
- Permet aux utilisateurs davantages une meilleures accessibilité peu n'importe l'appareil
- Flexibilité
- Adaptation
- Cohérant

## 5. Choix des fonctions CSS fluides

Permet a des meilleurs valeurs (spécifique) adaptatives selon la taille de l'écran 

EXEMPLE :
- CLAMP (min, preferred, max)
- CALC (unités fixes + fluides)
- min ou max (limitation)

ADVANTAGES :
- Restrictions
- Valeurs spécifiques
- Responsives

.about__title {
  font-size: clamp(2rem, 4vw, 2.5rem);
}
-Avoir une typographie reswponsive avec clamp

.services {
padding: 60px calc(20px + 8vw);
}
-Espacement fluide avec calc()

.contact__form-label {
width: min(100%, 313px);
}
-Largeur adaptative avec min()


## 6. Défis techniques rencontrés et vos solutions

Le premier défis majeur du projet est que je n'avais pas figma dev, ce qui rend les taches plus difficiles. Donc, je suis mis a faire le HTML avec les information très limiter et plus tards, le CSS.
Pour la partie de CSS, j'ai fait une partie de mon capacité et quand j'ai obtenus figma dev. J'aurai du modifier mon CSS, une autre fois, qui render les taches plus compliquer et diificile.

Le deuxieme defis est de rendre mon CSS responsive, donc c'était beaucoup de recherche et essaye erreur pour finalement reussi de rendre le projet responsive. Par exemple ajouter flex direction : row sur tout les contenants pour voir si ca marche ou pas.

## 7. Utilisation de l'intelligence artificiel.

J'ai utiliser l'intelligence artificielle pour donner et de faire des recherches sur un code et de corriger mon code en cas de faute d'ortographe. Par exemple comment flex display fonctionne, donner le code pour ajouter une image etc. Ceci respecte les contraintes et en meme temps maximizer l'éfficacité avec le temps et du comphrésion avec CHATGPT.

03 25 2026
Small fixes in your code
You had ;; → remove extra semicolon
Avoid repeating display: flex twice

03 23 2026
The calc() CSS function is a powerful tool that allows you to perform mathematical calculations directly within your CSS property values. It is primarily used to calculate lengths, percentages, angles, or times dynamically, enabling responsive layouts that mix different units (like pixels and percentages). 

03 20 2026
<img src="image_path.jpg" alt="Description of the image">





