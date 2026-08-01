# Plans de mise en œuvre et de déploiement (ébauche)

## Mise en œuvre (phases)

1. **Pilote** : un quartier ou un sous-domaine (ex. trafic + notifications) ; jeux de capteurs limités ; formation agents.  
2. **Extension** : utilitaires et sécurité ; intégration prestataires via portail ; durcissement IAM.  
3. **Generalisation** : urgence inter-services, montée en charge, procédures de continuité.

## Déploiement (logique)

- **Edge** : passerelles proches des capteurs (filtre, agrégation, reprise après coupure réseau).  
- **Cloud / datacenter** : bus, API, entrepôt, applications métier.  
- **Postes opérationnels** : consoles agents, SOC si applicable.

*Un diagramme de déploiement UML (nœuds + artefacts) sera ajouté dans `diagrams/06-deploiement/`.*

## CI/CD (indicatif)

Intégration continue des services exposés par la plateforme ; jeux de tests de contrat pour les producteurs d’événements IoT ; environnements **dev / recette / production** avec promotion contrôlée.
