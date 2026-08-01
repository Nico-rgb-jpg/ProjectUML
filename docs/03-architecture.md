# Architecture et fonctionnement (ébauche)

## Vue d’ensemble

Le système repose sur une **plateforme d’intégration** (`smartcity.platform`) qui collecte les données issues du terrain (capteurs, signalements), les expose via des **API** et un **bus d’événements**, et alimente des services de **corrélation**, d’**orchestration** (notamment urgence) et de **notification** vers le citoyen.

Les domaines métier (`traffic`, `utilities`, `safety`, `emergency`, `communication`) sont modélisés en **paquets** ; les **composants** matériels et logiciels sont détaillés dans `diagrams/05-composants/components-smart-city.puml`.

## Flux de données temps réel

1. Les capteurs et passerelles **edge** publient des lectures normalisées.  
2. Le **bus** distribue les flux aux consommateurs (règles, stockage série temporelle, tableaux de bord).  
3. Les décisions (alerte, dispatch) produisent des **mises à jour d’incident** et des **notifications**.

## Sécurité et confidentialité (lien avec le modèle)

- **IAM & audit** : composant dédié ; les accès des acteurs (citoyen, agent, prestataire) doivent apparaître dans les cas d’utilisation et les contraintes sur `CitizenProfile`.  
- **Données sensibles** : minimisation des attributs exposés aux prestataires ; traçabilité des accès (à détailler dans `docs/04-defis-et-nfr.md`).

## Prochaines complétions

- Ajouter un diagramme de **déploiement** (nœuds : edge, cloud, centre opérationnel).  
- Raffinier les classes par paquet (trafic, utilitaires, etc.) à partir des cas d’utilisation validés.
