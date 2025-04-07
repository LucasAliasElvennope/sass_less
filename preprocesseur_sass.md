# Introduction à Sass

Sass (Syntactically Awesome Stylesheets) est un préprocesseur CSS qui améliore l'écriture des feuilles de style en introduisant des fonctionnalités avancées. Il permet de rendre le code plus lisible, réutilisable et maintenable.

## Fonctionnalités principales de Sass

### 1. Variables
Les variables permettent de stocker des valeurs réutilisables, comme des couleurs, des polices ou des tailles.

```scss
$primary-color: #3498db;
$font-size: 16px;
```

### 2. Nidification (Nesting)

La nidification permet de structurer les styles de manière hiérarchique, ce qui rend le code plus lisible.

```scss
.nav {
  ul {
    list-style-type: none;
  }
  li {
    display: inline-block;
  }
}
```

### 3. Mixins

Les mixins permettent de créer des blocs de code réutilisables.

```scss
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
  -moz-border-radius: $radius;
  border-radius: $radius;
}

.box {
  @include border-radius(10px);
}
```

### 4. Héritage (Extend)

L’héritage permet à un sélecteur d’hériter des propriétés d’un autre sélecteur.

```scss
.message {
  padding: 10px;
  border-radius: 5px;
}

.error {
  @extend .message;
  background-color: red;
}
```

### 5. Opérations mathématiques

Sass permet de réaliser des calculs directement dans les styles.

```scss
.container {
  width: 100% / 3;
}
```

### 6. Partiels et importation

Les partiels permettent de diviser le CSS en plusieurs fichiers, facilitant ainsi l'organisation du code.

```scss
// _header.scss
.header {
  // styles
}

// main.scss
@import 'header';
```

### Conclusion

Sass est un outil puissant qui rend l'écriture des feuilles de style plus propre et plus facile à maintenir, surtout pour des projets de grande envergure.