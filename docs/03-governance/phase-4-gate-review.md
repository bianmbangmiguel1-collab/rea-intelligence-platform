# Porte de phase 4 — revue et autorisation de réalisation

**Statut :** décision du propriétaire enregistrée pour un sous-périmètre initial limité. Cette décision n'atteste pas que tous les prérequis d'intégration REA, de test sur cible réelle ou de production sont satisfaits.

## 1. Objet

La porte phase 4 sépare la conception de la réalisation. Elle peut autoriser un sous-périmètre contrôlé tout en laissant bloquées des dépendances non nécessaires à ce sous-périmètre. Chaque extension exige une revue et une autorisation distinctes.

## 2. État des critères généraux

| Critère | État | Périmètre / preuve |
| --- | --- | --- |
| Périmètre fonctionnel stable | Partiellement satisfait | Fondations locales mono-utilisateur seulement ; pilote complet et cas d'usage REA restent à arbitrer. |
| Révision REA immuable | Satisfaite comme référence documentaire | `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`. |
| Audit exhaustif des interfaces/capacités | Non satisfait | Le rapport documentaire identifie des sources générales ; catalogue et contrats exacts du pilote restent ouverts. |
| Conception fonctionnelle | Acceptée comme base documentaire | Ne constitue pas recette technique ni approbation de toutes fonctionnalités en production. |
| Conception sécurité/exploitation | Acceptée pour le périmètre restreint | Cible réelle, agent connecté, transport externe, IA et déploiement restent hors portée. |
| Dépendances/licences | Partiellement vérifiées | MIT REA-authored documenté ; dépendances exactes utilisées et tout outil tiers restent à vérifier avant adoption. |
| Critères de recette | Définis comme protocole | Aucun résultat de test n'est revendiqué ; recette phase 5 à exécuter. |
| Risques résiduels | Non clos globalement | Les risques de portée étendue restent ouverts et non acceptés par cette décision restreinte. |

## 3. Décision de sortie — sous-périmètre initial

À la demande explicite du propriétaire dans la conversation du 2026-11-12, la porte autorise uniquement la phase 5 locale/synthétique définie dans [`implementation-authorization.md`](../09-phase-5/implementation-authorization.md).

Cette décision n'autorise pas : l'exécution de REA, l'intégration opérationnelle à son catalogue, l'analyse de cible réelle, l'installation de nouveaux outils/dépendances, les transferts externes, ni le déploiement. La phase 4 demeure ouverte pour ces extensions tant que leurs critères spécifiques ne sont pas satisfaits.

## 4. Visa / traçabilité

- Décideur indiqué par le contexte de session : propriétaire du dépôt (`bianmbangmiguel1-collab`).
- Date de décision conversationnelle : 2026-11-12.
- Portée acceptée : fondations locales et tests sur fixtures synthétiques, sans nouvelles dépendances ni exécution REA.
- Source : demande explicite de réconcilier les consignes et de renseigner l'autorisation.
- Limite : validation documentaire de cette portée seulement ; aucun livrable ou résultat de recette n'est attesté par ce visa.
