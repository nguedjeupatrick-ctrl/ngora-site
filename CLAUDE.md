# Ngora Studio — site vitrine

Site one-page de Ngora Studio (Patrick, @rayaan.ng) : montage vidéo, gestion de réseaux,
vignettes, branding et sites web pour les marques. Tout le site tient dans `index.html`
(HTML + CSS + JS inline, aucune étape de build). Les médias sont dans `assets/`.

## Langue
- Toujours répondre et écrire le contenu du site en français.

## Structure
- `index.html` : nouveau site (rebranding 2026, DA « Studio éditorial »), une seule page avec scroll immersif.
  GSAP + ScrollTrigger (cdnjs), Lenis (unpkg) pour le défilement fluide, three.js r128 (cdnjs) pour le logo 3D chrome
  (forme tirée de `assets/3d/ngora-mark.json`, intégrée dans la page). Doit rester lisible sans JS et avec « réduire les animations ».
- `v1.html` : ancienne version (noir / chrome / orange), gardée pour référence.
- `assets/videos/` + `assets/posters/` : chaque vidéo `x.mp4` a son image fixe `x.jpg` (même nom).
- `assets/logos/`, `assets/insta/` (avant/après), `assets/dashboards/` (stats vérifiées), `assets/vignettes/`, `assets/stories/`, `assets/motion/`.
- `assets/sites/` : captures des sites web réalisés (Le Continent Store : https://lecontinentstore.github.io/).

## Identité visuelle (DA « Studio éditorial »)
- Papier `#EFEDE8` (fond), Encre `#111111` (texte), Cobalt `#2F3BFF` (accent unique), Pierre `#8B8A86` (texte discret).
- Polices : Inter Tight 800 (titres serrés, très gras) + Instrument Serif italique (mots clés, chiffres).
- Accroche : « Une image qui fait la différence. » (présence en ligne qui attire et qui convertit)
- Mission : aider les marques et les personnes qui ont un bon produit mais une image qui ne vend pas,
  sur tous les canaux (Instagram, TikTok, YouTube Shorts, LinkedIn, Facebook, site web), moins cher qu'une agence.
- Haut de page sombre (bulles) : intro = logo chrome 3D qui grossit puis se pose, accroche courte, showreel 3 vidéos, chiffres.
- Ordre : haut de page → Réalisations (showroom) → Ce que je fais → Sites web → Tarifs → Méthode → FAQ → Contact.
- Signatures : badge rond « Audit gratuit », curseur qui devient « Play »,
  logo Ngora en chrome 3D qui suit la souris, titres liquides au survol, traînée bleue du curseur.
- Réalisations « showroom » (inspiré de munrooftoprome.com) : carte vidéo au centre d'un arc, voisines floues, flèches,
  infos autour, bulles de couleur par marque, onglets de contenus. Services en grandes lignes : ligne active en bleu + aperçu (PC) ; cartes à faire glisser au doigt (mobile).

## Contact affiché sur le site
- E-mail : nguedjeupatrick@gmail.com · WhatsApp 06 49 28 83 90 (constante `WHATSAPP`, tous les liens `data-wa`).

## Mise en ligne
- Site public : https://nguedjeupatrick-ctrl.github.io/ngora-site/ (GitHub Pages, branche `main`, dossier racine).
- Tout ce qui est poussé sur `main` est en ligne 1 à 2 minutes plus tard.

## Statistiques de visite
- Umami (cloud.umami.is, sans cookie) : constante `UMAMI_ID` dans le dernier `<script>` d'`index.html` (vide = rien n'est envoyé).
- Événements : section-vue, defilement (25/50/75/100), clic-whatsapp (endroit, bouton), clic-lien-externe, clic-email, copie-email,
  clic-menu, showroom-fleche, showroom-marque, showroom-onglet, voir-plus-projets, service-ouvert, video-lue, temps-sur-page.
- Test local : `window.ngEvents` liste les événements même sans identifiant.

## Revue de novembre 2026 (déjà appliqué)
- Mobile : barre du haut 72 px (CTA masqué < 360 px), bouton audit au-dessus du showreel, badge masqué sur le contact,
  glisser du showroom seulement horizontal, pictogramme Play sur tactile, safe-area iPhone, logo 3D limité au 1er écran.
- Robustesse : intro calée sur le temps réel (NG_T0 / NG_LATE, jamais de clignotement si le CDN est lent), vidéos en pause hors
  écran (showreel, démo, showroom, services), verrou de défilement `html.ng-lock` (menu, lightbox), ancres `scroll-margin-top`
  + ouverture de la bonne marque / du bloc « Voir plus », flèches clavier sur les onglets, focus hors des cartes invisibles.
- SEO : title long, canonical, OG/Twitter absolus (assets/og.jpg = capture du nouveau haut de page), icônes carrées, JSON-LD
  ProfessionalService (adresse Presles), page `mentions-legales.html` liée en pied de page.
- Safari/perf (nov. 2026) : -webkit-backdrop-filter, html overflow-x:clip (iPhone), images en lazy + decoding async,
  logos PNG compressés (~1,1 Mo → 200 Ko), vidéos en faststart (index en début de fichier, à garder pour toute nouvelle vidéo).
- Reste à faire si besoin : supprimer le CSS mort (anciennes sections .marquee/.works/.motion/.fmt, ~4 Ko), témoignages
  clients (bloc à prévoir quand il y aura de vrais avis), identifiant Umami à renseigner.

## Façon de travailler (plusieurs PC)
- GitHub (`nguedjeupatrick-ctrl/ngora-site`) est la version de référence.
- Début de séance : récupérer la dernière version (`git pull`).
- Fin de séance : enregistrer et envoyer (`git commit` + `git push`).
- Tester sur mobile (largeur 375px) : le site doit rester sans défilement horizontal.
