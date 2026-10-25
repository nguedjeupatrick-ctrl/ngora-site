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
- Accroche : « Votre produit est bon. Votre image le dira. »
- Mission : aider les marques et les personnes qui ont un bon produit mais une image qui ne vend pas,
  sur tous les canaux (Instagram, TikTok, YouTube Shorts, LinkedIn, Facebook, site web), moins cher qu'une agence.
- Signatures : écran d'entrée automatique sans son (NGORA + travaux empilés qui deviennent le showreel), showreel du hero qui passe en plein écran, travaux en
  défilement horizontal, badge rond « Audit gratuit », curseur qui devient « Play »,
  logo Ngora en chrome 3D qui suit la souris, roue de vidéos qui tourne au scroll, titres liquides au survol, traînée bleue du curseur.

## Contact affiché sur le site
- E-mail : nguedjeupatrick@gmail.com · Instagram : @rayaan.ng · WhatsApp 04 49 28 83 90 (constante `WHATSAPP`, tous les liens `data-wa`).

## Façon de travailler (plusieurs PC)
- GitHub (`nguedjeupatrick-ctrl/ngora-site`) est la version de référence.
- Début de séance : récupérer la dernière version (`git pull`).
- Fin de séance : enregistrer et envoyer (`git commit` + `git push`).
- Tester sur mobile (largeur 375px) : le site doit rester sans défilement horizontal.
