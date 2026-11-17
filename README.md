# NeoMusic pour téléphone

La version téléphone de NeoMusic, pour l'appli Android de NeoDex. Elle garde la même bibliothèque que NeoMusic sur PC (même identifiant `neodex.music`) : tes playlists et tes favoris se synchronisent entre les deux.

*English version: [README.en.md](README.en.md)*

## Ce qu'elle garde du PC

Le même code que NeoMusic sur PC, avec ses 18 thèmes, la platine en pixel art, les pochettes, la barre de progression, les playlists, les favoris, la corbeille, les statistiques, les 33 succès, les niveaux, le mode sommeil et le widget.

## Ce qui change sur téléphone

- **Menu ☰** en haut à gauche : les playlists et la bibliothèque s'ouvrent dans un tiroir, qui se referme quand on choisit.
- La platine est en haut, la liste en dessous (fais défiler). **Un toucher** sur un morceau le lit, **un appui long** ouvre son menu.
- Le son passe par le lecteur YouTube de NeoDex et continue écran éteint ; la notification a lecture / pause, précédent et suivant.
- Les playlists « hors ligne » se lisent en ligne sur le téléphone ; le PC télécharge leurs fichiers comme d'habitude.
- Pas d'égaliseur, de balance, de spectre ni de forme d'onde (le son de YouTube ne passe pas par la page), pas de raccourcis clavier, pas d'import de fichier, d'artiste, de capsule ni de MuPlayer, pas de réveil, pas de recommandations (elles viennent de Deezer par le PC). Seuls les morceaux de YouTube se lisent.

## Autorisations

- **storage** : garder la bibliothèque ;
- **music** : la recherche YouTube et le lecteur de NeoDex sur téléphone ;
- **network:i.ytimg.com** : les pochettes des morceaux ;
- **widget** : le widget de l'accueil.

## Pour les développeurs

Le dépôt s'appelle comme celui du PC avec `-phone` à la fin. L'outil `catsync.js` (dossier `outils-publication`) lit sa dernière Release signée et l'écrit dans le champ `phone` du catalogue ; l'appli Android installe alors cette version au lieu de celle du PC. Le son passe par le service musique de NeoDex sur téléphone (`neo.musicSearch`, `neo.musicInfo`, `neo.musicPlayer`, `neo.onMusicPlayer`), décrit dans `NeoDyme/mobile/shell/neo-music.js`.
