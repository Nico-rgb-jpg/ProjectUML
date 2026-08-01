# Projet UML — Smart City

Documentation et diagrammes pour un système intégré de ville intelligente.

## Outil principal : draw.io

- **Fichier modèle** (plusieurs onglets) : [`diagrams/drawio/smart-city-projet.drawio`](diagrams/drawio/smart-city-projet.drawio) — ouvre-le avec [diagrams.net](https://app.diagrams.net/) ou l’extension Draw.io de l’IDE.  
- **Mode d’emploi** : [`docs/guide-drawio.md`](docs/guide-drawio.md) (formes UML, export PNG/PDF, structure des pages).

## Structure

- `docs/` — plan de travail, acteurs/scénarios, architecture, défis, déploiement, guide draw.io.  
- `diagrams/drawio/` — sources **`.drawio`** à rendre / exporter.  
- `diagrams/*/*.puml` — **référence optionnelle** (même contenu esquissé en PlantUML si tu veux t’en inspirer sans redessiner depuis zéro).

## Ordre de travail conseillé

1. `docs/01-plan-de-travail.md`  
2. Compléter les onglets du fichier draw.io dans l’ordre : **Paquetage → Composants → Cas d’utilisation → Classes → Séquence / Activité / État → Déploiement**.  
3. Exporter les figures pour le rapport (**Fichier → Exporter comme**).
