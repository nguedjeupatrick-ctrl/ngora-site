# Ngora Studio — site vitrine

Site one-page de Ngora Studio (Patrick, @rayaan.ng) : montage vidéo, gestion de réseaux,
vignettes, branding et sites web pour les marques. Tout le site tient dans `index.html`
(HTML + CSS + JS inline, aucune étape de build). Les médias sont dans `assets/`.

## Langue
- Toujours répondre et écrire le contenu du site en français.

## Structure
- `index.html` : 3 vues pilotées en JS (`data-view`) : `accueil`, `realisations`, `formats`.
- `assets/videos/` + `assets/posters/` : chaque vidéo `x.mp4` a son image fixe `x.jpg` (même nom).
- `assets/logos/` : logos clients ronds. `assets/insta/`, `assets/dashboards/` : preuves avant/après et stats.
- `assets/vignettes/`, `assets/stories/`, `assets/motion/` : vignettes YouTube, stories, motion design.

## Identité visuelle
- Fond noir `#0E0F10`, crème `#EDEBE6`, gris Nardo (`#7C7F82`, `#B4B7BA`), accent orange `#FF6B2C`.
- Polices : Anton (titres, majuscules) et Jost (texte), via Google Fonts.
- Effets : dégradé « chrome » (`--metal`), texture animée dans les titres, cartes `--panel`.

## Contact affiché sur le site
- E-mail : nguedjeupatrick@gmail.com · Instagram : @rayaan.ng · WhatsApp (bouton).

## Façon de travailler (plusieurs PC)
- GitHub (`nguedjeupatrick-ctrl/ngora-site`) est la version de référence.
- Début de séance : récupérer la dernière version (`git pull`).
- Fin de séance : enregistrer et envoyer (`git commit` + `git push`).
- Tester sur mobile (largeur 375px) : le site doit rester sans défilement horizontal.
