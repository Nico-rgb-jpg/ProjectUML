# Acteurs et scénarios (brouillon — à valider)

## Acteurs

| Acteur | Description courte |
|--------|-------------------|
| **Citoyen** | Usager des services (signalement, consultation, alertes reçues). |
| **Agent municipal** | Exploitation quotidienne (trafic, travaux, coordination). |
| **Prestataire** | Entreprise sous-traitante (maintenance capteurs, réseaux). |
| **Opérateur urgence** | SAMU/pompiers/police (selon périmètre du modèle). |
| **Administrateur SI** | Comptes, intégrations, supervision plateforme. |
| **Système externe** | Météo, cartographie, opérateurs télécom (optionnel). |

## Scénarios transversaux suggérés (pour séquences / activités)

1. **S1 — Alerte urgence** : détection (capteur / signalement) → validation → dispatch ressources → notification citoyens concernés.  
2. **S2 — Trafic adaptatif** : agrégation flux temps réel → recommandation / feux → information voyageurs.  
3. **S3 — Incident service public** : panne détectée ou signalement → work order prestataire → résolution → communication citoyenne.  

## Scénarios par domaine (pistes)

- **Trafic** : congestion, priorité véhicules d’urgence, travaux.  
- **Eau / électricité** : consommation anormale, coupure planifiée.  
- **Sécurité** : corrélation vidéo + capteurs, escalade.  
- **Communication** : diffusion d’information ciblée (géolocalisation / abonnements).

---

*Une fois validé, ces scénarios reçoivent des identifiants stables (S1, S2…) réutilisés dans les titres des diagrammes de séquence et d’activité.*
