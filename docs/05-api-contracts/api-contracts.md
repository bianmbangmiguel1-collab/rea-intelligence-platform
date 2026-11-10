# Contrats API de la plateforme — propositions

**Avertissement :** il s'agit d'une conception de notre API, pas d'endpoints REA. Ce document n'est pas encore un contrat implémentable : les schémas, versions, méthodes d'authentification, erreurs et règles de pagination restent à compléter.

## Conventions proposées

- API versionnée sous `/api/v1` avant implémentation.
- Identifiants opaques ; dates en UTC ; valeurs d'état explicitement énumérées.
- Toutes les opérations vérifient l'accès au workspace/projet côté serveur.
- Créations de jobs idempotentes avec une clé d'idempotence.
- Les réponses ne contiennent ni secrets d'agent ni URL d'objet persistante publique.
- Erreurs structurées : code stable, message sûr, identifiant de corrélation et détails de validation expurgés.

## Ressources conceptuelles

| Méthode | Route proposée | Contrat fonctionnel |
| --- | --- | --- |
| POST | `/api/v1/projects` | Créer un projet dans un workspace accessible. |
| GET | `/api/v1/projects/{projectId}` | Lire métadonnées et état du projet. |
| POST | `/api/v1/projects/{projectId}/targets` | Ajouter une cible avec provenance et autorisation. |
| POST | `/api/v1/analyses` | Créer une demande liée à projet/cible et au périmètre accepté. |
| GET | `/api/v1/analyses/{analysisId}` | Lire état, étapes et résumé autorisé. |
| POST | `/api/v1/analyses/{analysisId}/cancel` | Demander annulation ; réponse indique `requested`, non garantie d'arrêt immédiat. |
| GET | `/api/v1/analyses/{analysisId}/events` | Lire événements/progression avec curseur. |
| GET | `/api/v1/agents` | Lister uniquement les agents accessibles et leur fraîcheur. |
| POST | `/api/v1/agents/enrollments` | Démarrer un enrôlement contrôlé ; ne pas retourner de secret permanent. |
| POST | `/api/v1/resources/imports` | Déposer une ressource en quarantaine. |
| GET | `/api/v1/evidence/{evidenceId}` | Consulter une preuve selon les droits projet. |
| GET | `/api/v1/reports/{reportId}` | Consulter un rapport versionné et ses citations. |

## Création d'analyse — données requises conceptuellement

- `projectId`, `targetId` ;
- objectif et type de traitement demandé ;
- périmètre et identifiant de l'autorisation applicable ;
- catégories d'opérations et niveau d'approbation ;
- contraintes de transfert IA, conservation et budget ;
- sélection explicite d'agent, ou règle de sélection autorisée.

Le serveur doit revalider toutes les valeurs : aucune décision de permission n'est prise sur la seule base du frontend ou du modèle IA.

## Événements de suivi

Types internes proposés : `analysis.accepted`, `agent.assigned`, `step.started`, `approval.required`, `step.completed`, `evidence.recorded`, `warning`, `analysis.failed`, `analysis.cancelled`. Ils doivent inclure un identifiant d'événement dédupliquable, une date, l'identifiant du job et une provenance. Ils ne prétendent pas reproduire les événements MCP ou REA.

## Adaptateur REA

L'adaptateur traduit des messages internes vers le contrat réellement vérifié. Les paramètres d'appel sont validés contre les schémas de la révision épinglée. Les sorties brutes/erreurs sont conservées dans la mesure permise ; toute normalisation doit identifier les champs originaux et dérivés.

## Questions à fermer

Versionnement de l'API, format d'erreur, auth, pagination, événements temps réel (SSE/WebSocket), uploads pré-signés, limites de requêtes, idempotence, consentement IA, états et contrat exact de l'adaptateur REA.