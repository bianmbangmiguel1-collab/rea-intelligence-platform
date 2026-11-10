# Décisions de cadrage — pilote phase 3

**Statut :** périmètre, modèle de rôles et référence d'audit approuvés par le propriétaire du projet le 2026-11-10. Décision documentaire uniquement ; elle ne vaut ni validation technique de sécurité, ni autorisation d'exécuter REA ou d'analyser une cible réelle, ni autorisation de réalisation.

## 1. Périmètre minimal du pilote — approuvé

| Sujet | Décision approuvée | Limite |
| --- | --- | --- |
| Mode d'usage | Usage personnel, mono-propriétaire, sans comptes invités ni service multi-tenant | Pas de partage public ni d'accès inter-projets |
| Cibles | Systèmes de laboratoire ou appareils appartenant à l'utilisateur, ou couverts par une autorisation écrite explicite et limitée | Cette décision n'autorise aucune cible réelle ni aucun essai |
| Cas d'usage | Étude documentaire et expérimentation contrôlée ; opérations de lecture/non destructives uniquement après autorisation séparée et franchissement des portes applicables | Capacités REA à auditer avant toute intégration |
| Portée des tâches | Projet, cible, finalité, fenêtre de validité et exclusions doivent être explicitement consignés | Refus par défaut si une donnée de portée manque ou est ambiguë |
| Données | Données synthétiques ou de laboratoire de préférence ; données personnelles, secrets et données de tiers exclus du pilote initial | Aucune transmission IA autorisée ; mode sans IA par défaut |
| Plateforme initiale | Windows prioritaire, sous réserve d'audit et de vérification de compatibilité | Hypothèse à vérifier, pas une compatibilité déclarée |
| Multi-utilisateur | Exclu du pilote initial | Toute extension nécessite une nouvelle décision et une revue |

### Opérations admissibles uniquement après autorisation distincte

- Examiner la documentation et les sources de la révision REA épinglée, dans les limites de l'audit documentaire autorisé.
- Préparer des exigences et scénarios de vérification sans les exécuter.
- Après satisfaction des portes et autorisations applicables, envisager des opérations de lecture/non destructives sur un laboratoire explicitement autorisé et limité au périmètre approuvé.

Cette liste ne constitue pas une autorisation d'exécuter REA ou d'opérer sur une cible maintenant.

### Exclusions approuvées

- Cible publique, tierce ou non explicitement autorisée ; découverte ou extension automatique du périmètre.
- Action destructive ou persistante, exploitation, élévation de privilèges, contournement de contrôle, persistance, collecte/extraction d'identifiants, mouvement latéral ou déni de service.
- Commande système arbitraire, exécution automatique de fichiers/imports non fiables, ou action déclenchée par une sortie IA.
- Exécution REA, installation d'outils, analyse sur cible réelle, déploiement ou code applicatif avant satisfaction des portes et autorisation distincte.
- Transfert vers OpenRouter ou tout autre fournisseur IA avant décision explicite sur données, consentement, rétention et fournisseur.

## 2. Rôles et modèle d'approbation — approuvés

Le modèle de responsabilités et de séparation ci-dessous est approuvé pour le pilote. L'approbation du modèle ne désigne pas encore tous les titulaires individuels.

| Rôle | Responsabilité | Attribution pour le pilote |
| --- | --- | --- |
| Propriétaire de plateforme | Décisions globales, fournisseurs et suspension/révocation d'urgence | Peut être cumulé avec le propriétaire de projet en pilote personnel ; titulaire à consigner |
| Propriétaire de projet | Périmètre, cibles autorisées, finalité, données, permissions et approbations | Propriétaire du projet ; identité nominative à confirmer dans le registre des responsables |
| Opérateur | Prépare ou demande des tâches dans le périmètre accordé ; ne peut pas étendre ses droits | Peut être le propriétaire du projet dans le pilote personnel ; titulaire à consigner |
| Approbateur | Vérifie séparément les demandes sensibles et les autorisations de cible | Pour toute opération sur cible réelle, approbateur distinct privilégié ; sans séparation/approbation documentée, l'opération reste bloquée |
| Auditeur REA | Consigne les observations et sources de la révision approuvée | À désigner ; audit non effectué |

**Règle d'approbation :** aucun utilisateur ne s'accorde silencieusement une autorisation. Toute opération sur une cible réelle exige une preuve d'autorisation enregistrée et une approbation séparée, ou reste bloquée jusqu'à décision explicite. La faisabilité opérationnelle de cette séparation reste à préciser avant tout essai.

## 3. Référence REA à auditer — approuvée

- Dépôt source : [`morluto/rea`](https://github.com/morluto/rea)
- Branche observée : `main` (mutable, contexte seulement)
- Révision immuable approuvée : [`3345019fe1341db40c26af3463e136fcb7c7d11e`](https://github.com/morluto/rea/commit/3345019fe1341db40c26af3463e136fcb7c7d11e)
- Date d'observation : 2026-11-10 (métadonnées GitHub)
- Approbation : propriétaire du projet, 2026-11-10
- Statut : référence d'audit approuvée ; audit, revue de licence et compatibilité restent non effectués/non vérifiés.

Ne pas substituer le contenu courant de `main` à ce SHA. Toute autre révision exige une nouvelle décision et un rapport distinct ou une comparaison explicitement documentée.

## 4. Actions et validations encore ouvertes

| Action / décision | Statut | Responsable |
| --- | --- | --- |
| Périmètre du pilote, opérations et exclusions | Approuvé le 2026-11-10 | Propriétaire du projet |
| Modèle de rôles et d'approbation | Approuvé le 2026-11-10 | Propriétaire du projet |
| SHA de REA à auditer | Approuvé le 2026-11-10 | Propriétaire du projet |
| Consigner les titulaires nominatifs des rôles et désigner l'auditeur | À faire | Propriétaire du projet |
| Effectuer l'audit documentaire sourcé du SHA approuvé | À faire ; non exécuté | Auditeur à désigner |
| Autoriser toute opération ultérieure sur cible réelle | Non accordé ; décision séparée requise | Propriétaire du projet |
| Approbation globale des conceptions fonctionnelle/sécurité et passage phase 4 | En attente | Propriétaire du projet |

## 5. Conséquence sur les portes

Cette approbation fixe le périmètre du pilote et la révision de référence, mais ne clôt pas l'audit REA ni la phase 3. La phase 1 reste incomplète jusqu'à production et revue d'un audit sourcé ; la phase 3 reste en cours pour les décisions sécurité/exploitation restantes ; la phase 4 n'est pas franchie. Aucun développement, test sur cible, exécution REA ou déploiement n'est autorisé par cette décision documentaire.
