# Zone Rouge

FPS PvP en réseau entre potes, pour Windows (moteur Godot 4.5.1) : Match à mort par équipe, Mêlée générale, Désamorçage, mode classé, passe de combat gratuit, skins, manette…

## Télécharger le jeu

1. Ouvre la page **[Releases](https://github.com/Titan-CyberTech/Zone_Rouge/releases/latest)** et télécharge `ZoneRouge_Windows_vX.Y.Z.zip`.
2. Dézippe le dossier `ZoneRouge` dans un endroit où tu peux écrire (Bureau, Documents, disque de jeux…), **pas dans « Program Files »**.
3. Lance `ZoneRouge.exe`. Si Windows affiche « Windows a protégé votre ordinateur » (jeu non signé) : *Informations complémentaires* → *Exécuter quand même*.

Le fichier `LISEZ-MOI.txt` du dossier explique tout : commandes clavier et manette, jeu en réseau (LAN, VPN de jeu ou ports UDP 7777 / 7778), modes, économie, passe de combat.

Pour jouer ensemble, tout le monde doit avoir la même version : il suffit que chacun relance son jeu, il se met à jour tout seul.

## Nouveautés

- **3.3.1** : petites corrections (en spectateur à la manette, les boutons affichés sont ceux de la manette).
- **3.3** : écrans de chargement au lancement, à l'entrée en partie (carte, mode, règles) et au retour au menu, avec des astuces. La recherche de mise à jour est visible : le jeu écrit en petit ce qu'il lit sur GitHub et confirme s'il est à jour. En Désamorçage, vue d'ensemble de la carte avant la première manche ; en réseau, un PC plus lent à charger la carte ne rate plus le début de la partie.
- **3.2** : mises à jour automatiques depuis cette page.
- **3.1** : le jeu se joue entièrement à la manette (Xbox, PlayStation…), menus compris.
- **3.0** : Saison 1 « Lumières » : passe de combat gratuit (100 paliers), quêtes, niveaux de compte, mode classé, roulette des cartes.

## Mises à jour automatiques

À chaque lancement, l'écran de chargement vérifie la dernière Release publiée ici et affiche en petit ce qu'il lit :

```
› Lecture de api.github.com/repos/Titan-CyberTech/Zone_Rouge/releases/latest
› Réponse de GitHub : code 200 · 7 Ko lus en 240 ms
› Dernière version publiée : v3.3.1 « Zone Rouge 3.3.1 » — publiée le …
› Fichiers : ZoneRouge.pck (14,8 Mo, SHA-256) · ZoneRouge_Windows_v3.3.1.zip (45,5 Mo, SHA-256)
› Ta version : 3.3.1 -> le jeu est à jour
```

- En vert, tout va bien ; en jaune, une nouvelle version a été trouvée ; en rouge, un problème (hors ligne, GitHub indisponible…).
- Si une version plus récente existe, le jeu affiche ses nouveautés, la télécharge (le `.pck` seul quand c'est possible, sinon l'archive complète), vérifie sa taille et son empreinte SHA-256, l'installe puis redémarre tout seul.
- Le profil du joueur (argent, skins, statistiques) est toujours conservé. Sans connexion, le jeu démarre normalement avec la version installée.
- GitHub limite les vérifications à 60 par heure et par connexion Internet : au-delà, le jeu l'indique et démarre quand même.

## Publier une nouvelle version

1. Augmenter la version du jeu (`GAME_VERSION`) puis exporter « Windows Desktop ».
2. Créer une Release avec le tag **`v` + la version du jeu** (ex. `v3.3.1`), écrire les nouveautés (elles s'affichent dans le jeu) et joindre :
   - `ZoneRouge_Windows_v3.3.1.zip` : le dossier `ZoneRouge` complet (pour les nouveaux joueurs, et quand la version de Godot change) ;
   - `ZoneRouge.pck` : la mise à jour légère (~15 Mo).
3. Laisser l'étiquette « Latest » (pas « Pre-release »), puis publier : tous les joueurs reçoivent la mise à jour au lancement suivant.
