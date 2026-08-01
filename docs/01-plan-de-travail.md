# Plan de travail — Projet Smart City (UML)

## Objectif du livrable

Produire un **modèle UML cohérent** couvrant trafic, services publics, sécurité, urgence et communication, avec **documentation technique** et **pistes de mise en œuvre / déploiement**, en traitant explicitement intégration hétérogène, temps réel, sécurité, scalabilité et UX citoyenne.

---

## Phase 0 — Cadrage (0,5 à 1 j)

| Tâche | Résultat |
|--------|-----------|
| Liste des **acteurs** (citoyen, agent municipal, prestataire, opérateur urgence, admin SI, systèmes externes) | Table des acteurs + périmètre par domaine |
| **Domaines fonctionnels** et frontières | Base du diagramme de paquetage |
| **Scénarios prioritaires** (2–3 par domaine + 1 transversal) | Liste numérotée pour séquences / activités |
| **NFR** (non-fonctionnel) : latence, disponibilité, RGPD, chiffrement | Section « contraintes » dans la doc technique |

**Livrable :** ce document complété + `docs/02-acteurs-et-scenarios.md` (à remplir ensemble si besoin).

---

## Phase 1 — Vue d’ensemble architecturale

| Diagramme | Rôle | Fichier (PlantUML) |
|-----------|------|---------------------|
| **Paquetage** | Découper le modèle : Trafic, Utilities, Sécurité, Urgence, Communication, Plateforme données, Gouvernance & sécurité | `diagrams/01-paquetage/packages-smart-city.puml` |
| **Composants** | Logiciels + matériels (IoT, bus d’événements, API, bases, portail citoyen) | `diagrams/05-composants/components-smart-city.puml` |

**Livrable :** diagrammes + paragraphe dans `docs/03-architecture.md` reliant paquets ↔ composants.

---

## Phase 2 — Besoins et structure métier

| Diagramme | Rôle | Fichier |
|-----------|------|---------|
| **Cas d’utilisation** (par paquet + vue globale synthétique) | Interactions citoyens / municipalité / prestataires / système | `diagrams/02-cas-utilisation/` |
| **Classes** (par domaine + classes transverses : capteur, alerte, événement, identité, journal d’audit) | Objets : véhicules, capteurs, canaux, bases services | `diagrams/03-classes/` |

**Livrable :** un fichier `.puml` par sous-système majeur + un fichier `classes-transverses.puml`.

---

## Phase 3 — Comportement et orchestration

| Diagramme | Rôle | Exemples de scénarios |
|-----------|------|------------------------|
| **Séquence** | Enchaînement systèmes pour un cas réel | Alerte urgence (capteur → corrélation → dispatch → notification) ; pic trafic (feux adaptatifs) |
| **Activité** | Processus métier / décision | Traitement d’une alerte, demande citoyenne eau/électricité |
| **État** | Cycle de vie d’objets clés | États d’une `EmergencyAlert`, d’un `TrafficSegment`, d’un `WorkOrder` |

**Livrable :** `diagrams/04-comportement/` (minimum 2 séquences, 2 activités, 2 machines à états).

---

## Phase 4 — Documentation technique et déploiement

| Section | Contenu |
|---------|---------|
| Architecture | Contexte (C4 niveau contexte si utile), flux données temps réel, référence aux paquets/composants |
| Défis | Table : défi → décision d’architecture → mécanisme (API, bus, chiffrement, réplication, etc.) |
| Sécurité & confidentialité | Données sensibles, minimisation, rôles, traçabilité |
| **Plan de mise en œuvre** | Phases (pilote, extension), prérequis, formation |
| **Plan de déploiement** | Environnements (dev/stage/prod), IoT / edge, centre de données, CI/CD (schéma logique) |

**Livrable :** `docs/03-architecture.md`, `docs/04-defis-et-nfr.md`, `docs/05-plans-mise-en-oeuvre-deploiement.md`.

---

## Ordre recommandé (résumé)

1. Paquetage + composants (vision).  
2. Cas d’utilisation (besoins).  
3. Classes (structure).  
4. Séquence / activité / état (comportement sur scénarios validés).  
5. Documentation + plans (rédaction continue dès la phase 1).

---

## Critères de « terminé »

- Chaque **sous-système** du cahier des charges a au moins : cas d’utilisation, extrait de classes, et **une** interaction comportementale (séquence ou activité) le reliant aux autres.  
- Les **défis** (hétérogénéité, temps réel, sécurité, scalabilité, UX) sont **nommés** dans la doc et **reflétés** dans au moins un choix visible sur composants ou classes (ex. bus d’événements, agrégation, chiffrement).  
- Fichiers **`.drawio`** (ou export PDF/PNG) **versionnables** + instructions dans `README.md` et `docs/guide-drawio.md`. Les `.puml` restent une aide optionnelle.

---

## Prochaine séance (étape immédiate)

1. Valider la liste d’acteurs et 3 scénarios transversaux prioritaires.  
2. Compléter les cas d’utilisation du paquet **Urgence + Sécurité** (souvent le plus riche en séquence).  
3. Dériver les premières classes transverses (`SensorReading`, `Alert`, `Incident`, `Notification`).
