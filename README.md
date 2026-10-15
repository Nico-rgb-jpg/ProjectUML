# Projet UML · Smart City

Modélisation UML d'un système intégré de ville intelligente : gestion du trafic, services publics,
sécurité, urgences et communication avec les citoyens.

Le projet couvre les principales vues UML, de l'architecture générale jusqu'au comportement détaillé
d'un scénario d'urgence, avec une documentation technique qui accompagne chaque diagramme.

## Diagrammes réalisés

Tous les diagrammes sont dans un seul fichier draw.io à plusieurs onglets :
[`diagrams/drawio/smart-city-projet.drawio`](diagrams/drawio/smart-city-projet.drawio).

| Onglet | Diagramme | Ce qu'il montre |
|---|---|---|
| 01 | Paquetage | découpage en domaines : trafic, services publics, sécurité, urgence, communication, plateforme de données |
| 02 | Composants | capteurs IoT, passerelles, bus d'événements, API, bases de données, portail citoyen |
| 03 | Cas d'utilisation | interactions des citoyens, agents municipaux, prestataires, opérateurs d'urgence |
| 04 | Classes | classes transverses : capteur, alerte, événement, identité, journal d'audit |
| 05 | Séquence | scénario S1 : de la détection d'une alerte à la notification des citoyens |
| 06 | Activité | traitement d'une alerte, étape par étape |
| 07 | États | cycle de vie d'une alerte |
| 08 | Déploiement | répartition entre équipements de terrain, cloud et centre opérationnel |

Une version texte des principaux diagrammes est aussi disponible en **PlantUML** dans `diagrams/` (fichiers `.puml`).

## Documentation

| Fichier | Contenu |
|---|---|
| [`docs/01-plan-de-travail.md`](docs/01-plan-de-travail.md) | démarche suivie, phase par phase |
| [`docs/02-acteurs-et-scenarios.md`](docs/02-acteurs-et-scenarios.md) | acteurs du système et scénarios étudiés |
| [`docs/03-architecture.md`](docs/03-architecture.md) | architecture et circulation des données en temps réel |
| [`docs/04-defis-et-nfr.md`](docs/04-defis-et-nfr.md) | défis techniques et exigences non fonctionnelles (latence, disponibilité, RGPD, sécurité) |
| [`docs/05-plans-mise-en-oeuvre-deploiement.md`](docs/05-plans-mise-en-oeuvre-deploiement.md) | pistes de mise en œuvre et de déploiement |

## Ouvrir les diagrammes

- **En ligne** : ouvrir [app.diagrams.net](https://app.diagrams.net/), puis *Fichier > Ouvrir depuis > Appareil* et choisir le fichier `.drawio`.
- **Dans VS Code** : extension *Draw.io Integration*.
- **PlantUML** : extension *PlantUML* de VS Code, ou [plantuml.com](https://www.plantuml.com/plantuml).

## Compétences mobilisées

UML (paquetage, composants, cas d'utilisation, classes, séquence, activité, états, déploiement),
analyse des besoins, architecture logicielle orientée événements, prise en compte de la sécurité et du RGPD
dès la conception.

---

Projet d'école réalisé par **Nicolas Zogo Obame**, étudiant en Bachelor Ingénierie du Web à l'ESGI Grenoble.
