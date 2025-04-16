# cobbledex_autoscoreboard
Description

CobbledexScoreboard est un mod pour Minecraft qui génère une image de tableau de scores indiquant le nombre de Pokémons capturés par chaque joueur. Il fonctionne uniquement en conjonction avec le mod Cobbledex. Ce mod s'exécute côté serveur et n'a pas besoin d'être installé sur le client.
Fonctionnalités

    Génération automatique d'une image affichant les scores des joueurs.
    Actualisation régulière des statistiques de capture de Pokémon.
    Accès facile à l'image via un serveur web intégré.

Installation

    Installez le mod Cobbledex sur votre serveur.
    Placez le fichier .jar de CobbledexScoreboard dans le dossier mods de votre serveur.
    Lancez ou redémarrez votre serveur pour activer les mods.

Configuration

    Le fichier de configuration est créé automatiquement au premier démarrage du mod. Vous le trouverez dans le répertoire de configuration du serveur Minecraft, généralement dans le dossier config.
    Le fichier de configuration se nomme cobbledex-scoreboard.json.

Options de Configuration

json

{
  "port": 8080,
  "updateIntervalMinutes": 5,
  "imageTitle": "Scoreboard - Pokémon Capturés",
  "timeZone": "Europe/Paris",
  "autoDetectDataFolder": true,
  "manualDataFolderPath": ""
}

    port: Port sur lequel le serveur web écoutera. Par défaut, 8080.
    updateIntervalMinutes: Intervalle de temps en minutes pour mettre à jour l'image du scoreboard.
    imageTitle: Titre affiché en haut de l'image du scoreboard.
    timeZone: Fuseau horaire utilisé pour les timestamps.
    autoDetectDataFolder: Détecte automatiquement le dossier de données. Si false, manualDataFolderPath sera utilisé.
    manualDataFolderPath: Chemin manuel vers le dossier de données si la détection automatique est désactivée.

Accès à l'Image de Scoreboard

L'image générée est accessible via un serveur web intégré. Utilisez l'IP du serveur Minecraft et le port configuré pour accéder à l'image.
Exemple

    IP de connexion Minecraft: 122.244.17.217:27235
    Adresse de l'image: http://122.244.17.217:8080/scoreboard.png

Notes

    Assurez-vous que le port configuré est ouvert et accessible depuis l'extérieur si vous souhaitez accéder à l'image depuis une autre machine.
    En cas de modifications dans le fichier de configuration, redémarrez le serveur pour que les changements prennent effet.

