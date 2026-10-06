# Configuration MQTT — Simulation industrielle

Node-RED publie les données de la simulation vers le broker Mosquitto. Une application MQTT sur téléphone peut s’abonner aux topics ci-dessous.

## Mosquitto
mosquitto -c "%USERPROFILE%\mqtt-tp\mosquitto.conf" -v
Dans Node-RED :
Configuration MQTT
Pour utiliser la communication MQTT, il faut :
1. Créer un utilisateur et un mot de passe dans Mosquitto sur son PC.
2. Dans Node-RED, ouvrir le nœud MQTT out « Vers téléphone » et renseigner ces identifiants dans la configuration du broker.
3. Utiliser localhost comme serveur si Mosquitto et Node-RED fonctionnent sur le même PC, avec le port 1883.
4. Dans l’application MQTT du téléphone, renseigner l’adresse IPv4 du PC, le port 1883 et les identifiants créés.
## Topics utilisés

| Topic                    | Donnée publiée               |
| -------------------------| ---------------------------- |
| `usine/taux_defaut`      | Taux de défaut en %          |
| `usine/rejets`           | Nombre de produits rejetés   |
| `usine/stock_conforme`   | Nombre de produits conformes |
| `usine/produits_generes` | Nombre de produits générés   |
| `usine/emballes`         | Nombre de produits emballés  |


