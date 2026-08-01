# Utiliser draw.io (diagrams.net) pour le projet Smart City

## Installation et ouverture

- **En ligne** : [https://app.diagrams.net/](https://app.diagrams.net/) (aucune installation).  
- **Bureau** : [https://www.diagrams.net/](https://www.diagrams.net/) — même moteur, fichiers `.drawio` identiques.  
- Dans VS Code / Cursor : extension **Draw.io Integration** si tu préfères éditer dans l’IDE.

Ouvre le fichier **`diagrams/drawio/smart-city-projet.drawio`** : il contient plusieurs **onglets** (un par type de diagramme). Tu peux aussi dupliquer un onglet ou créer un fichier séparé par livrable si ton équipe préfère.

## Activer les formes UML

1. Menu **Plus de formes** (ou **+** dans le panneau de gauche).  
2. Coche **UML** (et éventuellement **Software** pour composants / déploiement).  
3. Valide : les palettes **UML** apparaissent (acteur, cas d’utilisation, classe, état, etc.).

Pour les **composants**, utilise la palette **UML** → *Component*, *Interface*, ou la section **Deployment** si tu fais un diagramme de déploiement.

## Correspondance avec ton cahier des charges

| Livrable | Formes / astuces draw.io |
|----------|---------------------------|
| **Paquetage** | Forme **Package** ; dépendances en tirets (`<<import>>` ou simple flèche pointillée selon ta notation cours). |
| **Cas d’utilisation** | **Actor**, **Use Case**, rectangle **System Boundary** (ou grand rectangle arrondi). |
| **Classes** | **Class** (3 compartiments) ; relations : association, agrégation, composition, héritage. |
| **Séquence** | Palette **UML** → lifelines et flèches synchrones / asynchrones ; ou modèle **Sequence** si proposé. |
| **Activité** | **Activity**, nœuds de décision (losange), fourches / jointures si besoin. |
| **État** | **State**, transitions, état initial / final. |
| **Composants** | **Component**, ports optionnels ; lien avec **Artifact** si tu sépares livrables logiciels. |
| **Déploiement** | Formes **Node**, **Artifact** ; flèches de communication. |

## Bonnes pratiques pour un rendu propre

- **Une intention par page** : un onglet = un diagramme (comme dans le fichier modèle).  
- **Grille + alignement** : active la grille ; utilise *Arranger → Align* pour un rendu lisible.  
- **Légende** : petit encadré pour expliquer couleurs ou stéréotypes (`<<service>>`, etc.) si le correcteur ne suit pas le même cours.  
- **Export** : **Fichier → Exporter comme → PNG ou PDF** pour le rapport ; vérifie la **résolution** (300 dpi si demandé).  
- **Nommage** : garde les mêmes noms d’éléments que dans `docs/02-acteurs-et-scenarios.md` (S1, S2…) pour que la doc et les figures se correspondent.

## Lien avec les fichiers PlantUML (optionnel)

Le dossier `diagrams/*/*.puml` sert de **référence** (contenu déjà esquissé). Tu peux **recopier** la structure dans draw.io à la main : draw.io ne lit pas le `.puml` nativement. Si tu veux tout centraliser dans draw.io uniquement, tu peux ignorer les `.puml` ou les supprimer plus tard.

## Prochaine étape

1. Compléter l’onglet **01 - Paquetage** avec tes vrais paquets et dépendances.  
2. Dupliquer la logique des scénarios S1–S3 en **séquence** et **activité** sur les onglets prévus.  
3. Ajouter un onglet **Déploiement** quand la vue composants est stable.
