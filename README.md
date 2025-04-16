# CobbledexScoreboard

## 📋 Description
CobbledexScoreboard est un mod Minecraft qui génère automatiquement une image du tableau des scores basée sur le nombre de Pokémon capturés par chaque joueur. Ce mod est conçu pour fonctionner exclusivement avec le mod Cobbledex, s'exécute côté serveur et ne nécessite aucune installation côté client.

## ✨ Fonctionnalités
- Génération automatique d'une image du tableau des scores
- Actualisation périodique des statistiques de capture
- Interface accessible via un serveur web intégré
- Configuration personnalisable
- Affichage multi-colonnes pour les serveurs avec beaucoup de joueurs
- Personnalisation complète des couleurs du tableau
- Option pour masquer la date de dernière mise à jour

## 🚀 Installation
1. Assurez-vous que le mod [Cobbledex](https://www.curseforge.com/minecraft/mc-mods/cobbledex) est installé sur votre serveur
2. Placez le fichier `.jar` de CobbledexScoreboard dans le dossier `mods` de votre serveur
3. Lancez ou redémarrez votre serveur pour activer le mod

## ⚙️ Configuration
Le fichier de configuration est automatiquement créé lors du premier démarrage du serveur. Vous le trouverez dans le dossier `config` de votre serveur Minecraft sous le nom `cobbledex-scoreboard.json`.

### Exemple de configuration
```json
{
  "port": 8080,
  "updateIntervalMinutes": 5,
  "imageTitle": "Scoreboard - Pokémon Capturés",
  "timeZone": "Europe/Paris",
  "autoDetectDataFolder": true,
  "manualDataFolderPath": "",
  "maxPlayers": 100,
  "rowsPerColumn": 10,
  "showLastUpdate": true,
  "colors": {
    "background": "#141414",
    "titleBackground": "#3232C8",
    "titleText": "#FFFFFF",
    "topPlayerText": "#FFFFFF",
    "firstPlaceBackground": "#FFD700",
    "secondPlaceBackground": "#C0C0C0",
    "thirdPlaceBackground": "#CD7F32",
    "text": "#FFFFFF",
    "footerText": "#FFFF00"
  }
}
```

### Options disponibles
| Option | Description | Valeur par défaut |
|--------|-------------|-------------------|
| `port` | Port d'écoute du serveur web | 8080 |
| `updateIntervalMinutes` | Fréquence de mise à jour du tableau (en minutes) | 5 |
| `imageTitle` | Titre affiché sur le tableau des scores | "Scoreboard - Pokémon Capturés" |
| `timeZone` | Fuseau horaire pour les horodatages | "Europe/Paris" |
| `autoDetectDataFolder` | Activation de la détection automatique du dossier de données | true |
| `manualDataFolderPath` | Chemin manuel vers le dossier de données (si `autoDetectDataFolder` est désactivé) | "" |
| `maxPlayers` | Nombre maximum de joueurs à afficher sur le tableau | 100 |
| `rowsPerColumn` | Nombre de lignes par colonne | 10 |
| `showLastUpdate` | Afficher ou masquer la date et l'heure de dernière mise à jour | true |
| `colors` | Dictionnaire des couleurs du tableau (format hexadécimal) | Voir exemple |

### Personnalisation des couleurs
Le tableau des scores peut être entièrement personnalisé en modifiant les couleurs suivantes :
- `background` : Couleur de fond générale du tableau
- `titleBackground` : Couleur de fond du titre
- `titleText` : Couleur du texte du titre
- `topPlayerText` : Couleur du texte pour les joueurs aux 3 premières places
- `firstPlaceBackground` : Couleur de fond pour la première place
- `secondPlaceBackground` : Couleur de fond pour la deuxième place
- `thirdPlaceBackground` : Couleur de fond pour la troisième place
- `text` : Couleur du texte pour les autres joueurs
- `footerText` : Couleur du texte du pied de page (date de mise à jour)

### Mise en page du tableau
La mise en page du tableau est automatiquement ajustée en fonction des paramètres `maxPlayers` et `rowsPerColumn` :
- Le nombre de colonnes est calculé automatiquement en fonction du nombre de joueurs et du nombre de lignes par colonne
- Si vous avez beaucoup de joueurs, augmentez `rowsPerColumn` pour créer des colonnes plus hautes
- Pour limiter le nombre de joueurs affichés, ajustez la valeur de `maxPlayers`

## 🖼️ Accès à l'image
Pour accéder à l'image du tableau des scores :
- IP de connexion Minecraft : `122.244.17.217:27235`
- URL de l'image : `http://122.244.17.217:8080/scoreboard.png`

## ⚠️ Notes importantes
- Le port configuré doit être accessible depuis l'extérieur si vous souhaitez que l'image soit visible en dehors de votre réseau local
- N'oubliez pas de redémarrer votre serveur après toute modification de la configuration
- Vérifiez que votre pare-feu autorise les connexions sur le port configuré
- Si le mod ne fonctionne pas correctement, veuillez contacter le support de votre hébergeur de serveur

## 🔄 Compatibilité
- Version de Minecraft supportée : 1.20.1
- Requiert le mod [Cobbledex](https://www.curseforge.com/minecraft/mc-mods/cobbledex)
