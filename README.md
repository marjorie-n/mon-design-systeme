# Mon design system

Le design system de mon site de web designer, [marjorie-ngoupende.netlify.app](https://marjorie-ngoupende.netlify.app/) : les couleurs, la typographie, les composants et les règles d’accessibilité qui donnent au site son identité.

Un design system, c’est la boîte à outils d’un site. Il garantit que chaque page reste claire, cohérente et accessible à tous, quelle que soit la personne qui la construit.

**Voir la présentation en ligne :** [marjorie-n.github.io/mon-design-systeme](https://marjorie-n.github.io/mon-design-systeme/)

## Ce que contient ce dépôt

| Dossier ou fichier | Contenu |
| --- | --- |
| `index.html` | La page de présentation, publiée avec GitHub Pages. |
| `tokens/tokens.json` | Toutes les valeurs du design system : couleurs pour les trois thèmes, styles de texte, espacements, arrondis, traits, largeurs. |
| `css/tokens.css` | Les mêmes valeurs en variables CSS, prêtes à l’emploi. |
| `css/composants.css` | Les styles des composants : bouton, carte, pilier, accroche, en-tête, liens d’évitement, bloc contact, pied de page. |
| `exemples/index.html` | Une page qui montre chaque composant, avec un sélecteur de thème. |
| `docs/charte.md` | La charte : principes, ton, couleur, typographie, mise en page, accessibilité, logo. |
| `docs/composants.md` | Le mode d’emploi de chaque composant : quand l’utiliser, quoi fournir, quoi éviter. |
| `assets/logo.png` | Mon logo, le monogramme « mn ». |

## Trois thèmes

- **Clair** : le thème par défaut.
- **Sombre** : appliqué automatiquement si l’appareil est réglé en mode sombre, ou au choix de la personne.
- **Contraste élevé** : pour les personnes malvoyantes ou gênées par les teintes douces. Chaque texte atteint au moins 7:1 (niveau AAA des WCAG) et les blocs se distinguent par des bordures nettes.

Le thème se choisit avec l’attribut `data-theme` sur la balise `html` : `light`, `dark` ou `contraste`. Sans attribut, le site suit le réglage de l’appareil.

## Utiliser le design system

Chargez les deux feuilles de style, dans cet ordre :

```html
<link rel="stylesheet" href="css/tokens.css">
<link rel="stylesheet" href="css/composants.css">
```

Puis écrivez vos pages avec les classes des composants :

```html
<a class="bouton" href="#contact">Parlons de votre projet</a>

<ul class="grille">
  <li class="carte">
    <h3>Diagnostic d’accessibilité</h3>
    <p>Vérification de premier niveau de votre site.</p>
    <p class="meta">Accessibilité · RGAA</p>
  </li>
</ul>
```

Pour utiliser une couleur dans votre propre CSS, passez toujours par sa variable, par exemple `color: var(--texte-doux);` ou `background: var(--fond-accent);`. Ainsi, elle s’adapte toute seule aux trois thèmes.

## Accessibilité

- Tous les textes atteignent au moins 4,5:1 de contraste en clair et en sombre (niveau AA), et 7:1 en contraste élevé (niveau AAA).
- Le focus clavier est toujours visible : un contour plein de 3 pixels.
- Les composants fonctionnent au clavier et avec un lecteur d’écran.
- Le mode contraste élevé de Windows et la réduction des animations sont pris en charge.

Le détail des contrastes, thème par thème, est sur la [page de présentation](https://marjorie-n.github.io/mon-design-systeme/#couleurs).

## Licence

Le code de ce dépôt (CSS, valeurs, exemples) est sous [licence MIT](LICENSE) : vous pouvez le réutiliser, y compris pour un projet commercial, en gardant la mention de copyright. Mon nom et mon logo ne sont pas concernés : ils restent ma propriété.

## À propos

Je suis Marjorie Ngoupende, web designer à Toulon, spécialisée en UX/UI, WordPress et accessibilité numérique.

- Site : [marjorie-ngoupende.netlify.app](https://marjorie-ngoupende.netlify.app/)
- LinkedIn : [marjorie-ngoupende](https://www.linkedin.com/in/marjorie-ngoupende/)
- YouTube : [@marjorie_ngoupende](https://www.youtube.com/@marjorie_ngoupende)
