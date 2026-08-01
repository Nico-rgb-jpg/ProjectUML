# Défis, NFR et arbitrages (ébauche)

| Défi | Exigence | Réponse architecturale (dans les diagrammes) |
|------|-----------|-----------------------------------------------|
| Systèmes hétérogènes | Interopérabilité | Bus d’événements, API Gateway, normalisation (`NormalizedEvent` côté séquence) |
| Temps réel | Latence, volumétrie | Edge + stream processing (composants `Bus`, `Rules`) |
| Sécurité & confidentialité | RGPD, audit | `IAM`, consentements sur `CitizenProfile`, journal d’audit |
| Scalabilité & fiabilité | Montée en charge, HA | Découplage par bus, stockage analytique séparé (`DataStore`) |
| UX citoyenne | Clarté, canaux multiples | Cas d’utilisation citoyen, service `Notification` multi-canal |

Cette table sera enrichie lors du choix concret des technologies (Kafka, MQTT, etc.) — le modèle UML peut rester **agnostique** en les nommant comme stéréotypes ou notes.
