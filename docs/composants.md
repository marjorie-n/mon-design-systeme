# Composants
Chaque composant s’écrit en HTML avec les classes de `css/composants.css`. Exemples complets : `exemples/index.html`.

## Bouton

Bouton d'action : lien stylé en bouton, pour l'action principale d'une section (contacter, écrire).

- **Primaire** (`.bouton`) : fond `accent`, texte `accent-texte`, style `bouton`, `radius-sm`, padding `pad-bouton-y` × `space-6`.
- **Secondaire** (`.bouton .bouton-secondaire`) : transparent, texte et contour `accent` (`trait-controle`).
- Au survol, le libellé se souligne ; au focus, contour `focus` de 3px décalé de 3px.
- En mode contraste élevé, un contour `ButtonText` reste visible.

**À fournir** : un `<a class="bouton" href="…">` (ou un `<button class="bouton">` pour une action dans la page) et un libellé explicite à l'infinitif ou à l'impératif (« Parlons de votre projet », « Écrire un e-mail »).

**À éviter** : plus d'un bouton primaire par bloc ; « Cliquez ici » ; un bouton sans texte.

## Carte

Carte de service, de réalisation ou de ressource, dans une grille fluide.

- Fond `fond`, contour `trait-fin` en `bordure`, filet `trait-carte` en `accent` en bas, padding `space-6`.
- Titre h3 en `titre-carte` (lien éventuel vers le projet), description en `texte-doux`, ligne `meta` en bas (étiquettes séparées par « · » ou date).
- Une capture optionnelle peut s'afficher en haut, à fond perdu (`<img>` en premier enfant, avec un `alt` descriptif).
- Les cartes se placent dans une liste `.grille` (`<ul>`), minimum 16rem, écart `space-5`.

**À fournir** : un `<li class="carte">` avec un `h3`, un paragraphe, et si besoin un `p.meta`.

**À éviter** : un lien sur toute la carte (on met le lien sur le titre) ; plus de trois étiquettes dans la ligne meta.

## Pilier

Pilier : un grand domaine d'expertise présenté en deux lignes, avec le filet accent à gauche.

- Filet `trait-accent` (6px) en `accent` à gauche, padding gauche `space-5`.
- Titre en `titre-section`, texte en `texte-doux` avec un ou deux mots-clés en `strong`.
- Se placent dans une liste `.piliers`, minimum 18rem, écart `space-6`.

**À fournir** : un `<li class="pilier">` avec un titre et une phrase.

**À éviter** : plus de trois piliers ; des paragraphes longs (c'est un résumé).

## Accroche

Bandeau d'accroche en haut de page : la promesse, le contexte, une action.

- Fond `fond-accent`, padding vertical `space-16`.
- Titre h1 en `titre-accroche` (taille fluide de 2rem à 3.2rem, largeur `mesure-titre`), les mots-clés en `strong` couleur `accent-fonce`.
- Chapô en `chapo` et `texte-doux`, largeur `mesure-texte`, puis un `Bouton` primaire.
- Sur le site, une photo portrait (ratio 4/5, `radius-md`, liseré `trait-accent` en bas) se place à droite au-delà de `point-rupture`, au-dessus sur mobile. Elle n'est pas reprise dans cet aperçu.

**À fournir** : le titre (une phrase, deux mots forts), un chapô de deux ou trois phrases, le libellé du bouton.

**À éviter** : un deuxième h1 ; un carrousel ; du texte dans une image.

## En-tête

En-tête du site : la marque à gauche, le menu principal à droite, un trait fin en bas.

- Logo (`assets/Logos/logo.png`) à 3.5rem avec `radius-logo`, `alt=""` car le nom suit ; nom en `nom-marque`, sous-titre en `corps-pied` et `texte-doux`.
- Menu dans un `<nav aria-label="Menu principal">`, liens en `lien-nav` couleur `accent`, sans soulignement (souligné au survol), écart `space-6`.
- Bas de l'en-tête : `trait-fin` en `bordure`. Le tout passe à la ligne sur mobile (flex-wrap).

**À fournir** : le lien d'accueil, quatre ou cinq ancres de menu au plus.

**À éviter** : un menu caché derrière une icône sur grand écran ; un logo seul sans nom.

## Liens d’évitement

Liens d'évitement : premiers éléments de la page, invisibles jusqu'à ce qu'ils reçoivent le focus clavier.

- Placés hors écran (`top: -5rem`), ils apparaissent en haut à gauche au focus : fond `accent`, texte `accent-texte`, `radius-sm`, padding `pad-evitement-y` × `space-4`.
- Deux liens : « Aller au contenu » (vers `main`, avec `tabindex="-1"`) et « Aller au pied de page ».

**À fournir** : une liste `<ul class="evitement">` en tout début de `body`, des cibles avec un `id`.

**À éviter** : `display: none` (le lien ne serait plus atteignable) ; plus de trois liens.

L'aperçu montre le lien dans son état visible (focus).

## Bloc contact

Bloc contact en fin de page : une invitation, un délai de réponse, un bouton et les réseaux.

- Fond `fond-accent`, padding `space-8`, `radius-sm`, deux colonnes fluides (minimum 18rem).
- Titre en `titre-section`, texte en `texte-doux`, `Bouton` primaire, puis la liste des réseaux (liens texte, écart `space-6`) avec un `aria-label`.

**À fournir** : le titre (« Un projet ? Parlons-en. »), une phrase de réassurance, l'adresse e-mail, les liens des réseaux.

**À éviter** : un formulaire sans étiquettes visibles ; des icônes de réseaux sans nom.

## Pied de page

Pied de page, toujours sombre : présentation, paramètres d'affichage, mentions légales, accessibilité.

- Fond `pied`, texte `pied-texte` en `corps-pied`, liens `pied-lien`, focus `focus-pied`. Titres en `titre-pied`, sous-titres en `sous-titre-pied`.
- Colonnes fluides (minimum 16rem, écart `space-8`), puis une ligne de liens séparée par un `trait-fin` en `pied-filet`.
- **Choix du thème** : quatre boutons radio (clair, sombre, contraste élevé, système ; « Contraste élevé » est à ajouter au site) dans un `fieldset` avec `legend` ; contour `trait-controle` en `pied-texte`, pastille `pied-lien` quand coché. Le bloc n'apparaît que si JavaScript fonctionne.
- **Adapter l'affichage** : un `details`/`summary` qui explique comment agrandir, renforcer les contrastes ou écouter la page.

**À fournir** : les mentions légales (éditrice, SIRET, hébergeur), un moyen de signaler un problème d'accès.

**À éviter** : des liens en `accent` sur `pied` (contraste insuffisant) ; supprimer la déclaration d'accessibilité.
