# Zone Rouge

FPS PvP en réseau entre potes, pour Windows (moteur Godot 4.5.1) : Match à mort par équipe, Mêlée générale, Désamorçage, mode classé, passe de combat gratuit, skins, manette…

## Télécharger le jeu

1. Ouvre la page **[Releases](https://github.com/Titan-CyberTech/Zone_Rouge/releases/latest)** et télécharge `ZoneRouge_Windows_vX.Y.Z.zip`.
2. Dézippe le dossier `ZoneRouge` dans un endroit où tu peux écrire (Bureau, Documents, disque de jeux…), **pas dans « Program Files »**.
3. Lance `ZoneRouge.exe`. Si Windows affiche « Windows a protégé votre ordinateur » (jeu non signé) : *Informations complémentaires* → *Exécuter quand même*.

Le fichier `LISEZ-MOI.txt` du dossier explique tout : commandes clavier et manette, jeu en réseau (LAN, VPN de jeu ou ports UDP 7777 / 7778), modes, économie, passe de combat.

## Mises à jour automatiques

Depuis la version 3.2, le jeu vérifie à chaque lancement la dernière Release publiée ici. Si une version plus récente existe, il affiche les nouveautés, la télécharge (le `.pck` seul quand c'est possible, sinon l'archive complète), vérifie sa taille et son empreinte SHA-256, l'installe puis redémarre tout seul. Le profil du joueur (argent, skins, statistiques) est toujours conservé. Sans connexion, le jeu démarre normalement.

## Publier une nouvelle version

1. Augmenter la version du jeu (`GAME_VERSION`) puis exporter « Windows Desktop ».
2. Créer une Release avec le tag **`v` + la version du jeu** (ex. `v3.3.0`), écrire les nouveautés (elles s'affichent dans le jeu) et joindre :
   - `ZoneRouge_Windows_v3.3.0.zip` : le dossier `ZoneRouge` complet (pour les nouveaux joueurs, et quand la version de Godot change) ;
   - `ZoneRouge.pck` : la mise à jour légère (~15 Mo).
3. Ne pas cocher « pre-release », puis publier : tous les joueurs reçoivent la mise à jour au lancement suivant.
