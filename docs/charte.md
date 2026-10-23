# Charte de la marque

Des sites web simples et accessibles à tous. Ce système décrit l'identité de Marjorie Ngoupende, web designer à Toulon (UX/UI, WordPress, accessibilité numérique) : une marque claire, pédagogique et sobre, construite autour d'une seule couleur, le bleu-vert profond du logo `accent` (#004952).

## Principes

- **Clarté d'abord.** Une idée par bloc, des titres qui disent ce que la section contient, des phrases courtes.
- **Accessible par défaut.** Chaque choix visuel respecte le RGAA et les WCAG niveau AA : contrastes vérifiés, focus visible, navigation au clavier, thèmes clair, sombre et contraste élevé, respect de `prefers-reduced-motion` et du mode contraste élevé.
- **Une couleur, des filets.** La marque se reconnaît à sa teinte `accent` et à ses filets épais (`trait-accent`, `trait-carte`), pas à des ombres ni à des dégradés.

## Contenu et ton

- **Voix.** Marjorie parle en « je » ; elle vouvoie les visiteurs (« Parlons de votre projet », « Je vous réponds sous 48 heures »). Le « nous » sert seulement à inviter : « Concevons des sites web simples et accessibles à tous. »
- **Ton.** Chaleureux et pédagogique : on explique sans jargon, on rassure, on montre le bénéfice pour le visiteur (« vos visiteurs trouvent vite ce qu’ils cherchent »). Quand un terme technique est nécessaire (RGAA, NVDA, Figma), il est accompagné d'une explication simple.
- **Casse.** Majuscule seulement en début de titre et aux noms propres : « Mes réalisations », « Ressources sur l’accessibilité ».
- **Typographie française.** Apostrophe typographique (’), guillemets « » avec espaces, point médian « · » pour séparer des étiquettes (« Refonte · WordPress · Accessibilité »), dates courtes (« 10 juil. 2026 »).
- **Libellés d'action explicites**, compréhensibles hors contexte : « Écrire un e-mail », « Voir toutes mes vidéos », « Signalez-le-moi ». Jamais « Cliquez ici » ni « En savoir plus » seul.
- **Pas d'emoji**, ni dans les titres ni dans les boutons.
- **Mots mis en valeur** avec `strong`, deux ou trois par paragraphe au plus (« simples », « accessibles à tous », « tout le monde »).

## Couleur

- Pose le texte courant en `texte` sur `fond`, `fond-alt` ou `fond-accent` ; le texte secondaire (chapô, intros, descriptions, métadonnées) en `texte-doux`.
- Alterne les sections entre `fond` et `fond-alt` pour rythmer la page ; réserve `fond-accent` au bandeau d'accroche et au bloc contact.
- Utilise `accent` pour les liens, le fond des boutons et les filets. Le texte posé sur `accent` est toujours `accent-texte` (blanc en clair, presque noir en sombre, car l'accent s'éclaircit).
- Le pied de page est toujours sombre : fond `pied`, texte `pied-texte`, liens `pied-lien`, focus `focus-pied`.
- `bordure` est un trait décoratif à faible contraste : ne l'utilise jamais seul pour délimiter un champ ou un contrôle.
- Trois thèmes sont livrés : `light` par défaut, `dark` selon `prefers-color-scheme` ou le choix de la personne, et `contraste` (attribut `data-theme` sur `html`, mémorisé localement).

### Thème « Contraste élevé »

- Pour les personnes malvoyantes ou gênées par les teintes douces. Il s'ajoute aux thèmes clair et sombre et ne les remplace pas.
- Chaque texte atteint au moins 7:1 (WCAG AAA) : `texte` en noir, `texte-doux` en #1b1f22, l'`accent` fonce à #003a42, `pied-lien` s'éclaircit à #bfeaef sur un `pied` presque noir.
- Les surfaces se distinguent par des bordures `bordure` (#4b5357) d'au moins 3:1, pas seulement par leur fond : contour de 2px autour des cartes et du bloc contact, trait sous l'accroche. Les liens du menu restent soulignés.
- Propose-le dans le choix du thème du pied de page, comme quatrième option : « Contraste élevé ». Il ne remplace pas le mode contraste élevé de Windows (`forced-colors`), qui reste pris en charge.

## Typographie

- Une seule famille, celle du système (`--font-sans` : system-ui, Segoe UI, Roboto, Arial) : rapide, lisible, familière à chaque visiteur. Aucune police à télécharger.
- Corps de texte à 18px (`corps`), interligne 1.6 ; titres en gras, interligne 1.25.
- Hiérarchie : `titre-accroche` (h1, fluide de 2rem à 3.2rem) → `titre-section` (h2) → `titre-carte` (h3). Un seul h1 par page, pas de niveau sauté.
- `chapo` pour le paragraphe d'accroche, `meta` pour les étiquettes et dates en bas de carte.
- Limite la longueur des lignes : `mesure-texte` (44rem) pour les paragraphes, `mesure-titre` (48rem) pour le h1.

## Espacement et mise en page

- Conteneur centré de `conteneur-max` (70rem) avec une gouttière `space-4` (1rem) de chaque côté.
- Chaque section a un padding vertical `space-14` ; le bandeau d'accroche `space-16`.
- Grilles fluides `auto-fit` : cartes de 16rem minimum espacées de `space-5`, piliers de 18rem minimum espacés de `space-6`. Pas de point de rupture sauf pour l'accroche (`point-rupture`, 52rem), qui passe alors sur deux colonnes avec le portrait à droite.
- Sur mobile, le portrait passe au-dessus du texte et réduit à 9rem.

## Formes, traits et états

- Angles à peine arrondis : `radius-sm` pour les boutons et le bloc contact, `radius-md` pour la photo, `radius-logo` pour le logo.
- Pas d'ombre portée. La profondeur vient des fonds (`fond-alt`, `fond-accent`) et des filets : `trait-accent` (6px) à gauche des piliers et sous le portrait, `trait-carte` (4px) en bas des cartes, `trait-fin` pour les contours.
- **Focus** : contour plein `trait-focus` (3px) en `focus`, décalé de 3px, sur tous les éléments interactifs ; `focus-pied` dans le pied de page. Ne jamais le supprimer.
- **Survol** : les liens épaississent leur soulignement (2px) ; les boutons et liens de menu se soulignent. Pas de changement de couleur seul.
- **Mouvement** : seulement le défilement doux vers les ancres, désactivé avec `prefers-reduced-motion`.
- **Contraste élevé Windows** (`forced-colors`) : les boutons gardent un contour `ButtonText`, les radios cochés une pastille `CanvasText`.

## Accessibilité à intégrer partout

- Deux liens d'évitement en tout début de page : « Aller au contenu », « Aller au pied de page ».
- Landmarks `header`, `nav` (avec `aria-label`), `main`, `footer` ; sections nommées par leur titre (`aria-labelledby`).
- Image décorative : `alt=""` (le logo à côté du nom) ; image informative : `alt` qui dit ce qu'elle montre (« Portrait de Marjorie Ngoupende »).
- Une langue étrangère est signalée (`lang="en"` sur « Netlify, Inc. », « NVDA »).
- Le pied de page propose un bloc dépliable « Adapter l’affichage avec votre navigateur » et le choix du thème.

## Logo et iconographie

- Le logo est le monogramme « mn » en écriture manuscrite blanche sur un carré `accent` (#004952) : `assets/Logos/logo.png` (112 × 112 px). Affiche-le à 3.5rem avec `radius-logo`, à côté du nom en `nom-marque` ; il est alors décoratif (`alt=""`).
- Il n'existe pas de version vectorielle (SVG) du logo pour l'instant.
- Pas de jeu d'icônes : le site s'appuie sur des liens textuels explicites. N'ajoute pas d'icône sans libellé texte.
