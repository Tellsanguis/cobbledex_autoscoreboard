# CobbledexScoreboard

## 📋 Description
CobbledexScoreboard est un mod Minecraft qui génère automatiquement une image du tableau des scores basée sur le nombre de Pokémon capturés par chaque joueur. Ce mod est conçu pour fonctionner exclusivement avec le mod Cobbledex, s'exécute côté serveur et ne nécessite aucune installation côté client.

## ✨ Fonctionnalités
- Génération automatique d'une image du tableau des scores
- Actualisation périodique des statistiques de capture
- Interface accessible via un serveur web intégré
- Configuration personnalisable

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
  "manualDataFolderPath": ""
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
